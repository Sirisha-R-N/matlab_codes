% Read the blurry image
blurryImage = imread('blurry_image.jpg');

% Convert the image to grayscale if it is a color image
if size(blurryImage, 3) == 3
    blurryImage = rgb2gray(blurryImage);
end

% Display the original blurry image
figure;
imshow(blurryImage);
title('Original Blurry Image');

% Define the point spread function (PSF)
% The PSF is the blurring kernel. Here, we assume a simple motion blur.
len = 21;  % Length of the motion
theta = 11; % Angle of the motion
psf = fspecial('motion', len, theta);

% Estimate the noise-to-signal power ratio (NSR)
% The NSR is usually estimated from the image itself or provided.
estimated_nsr = 0.01; % Adjust this value based on the noise level in the image

% Perform Wiener deconvolution
deblurredImage = deconvwnr(blurryImage, psf, estimated_nsr);

% Display the deblurred image
figure;
imshow(deblurredImage);
title('Deblurred Image');

% Save the deblurred image
imwrite(deblurredImage, 'deblurred_image.jpg');
