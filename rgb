% Define the folder containing your images
folder = '"C:\Users\siris\OneDrive\Documents\MATLAB\Color 0"';
% Get a list of all image files in the folder
fileList = dir(fullfile(folder, '*.jpg')); % Update file extension as needed

% Initialize variables to store RGB values
rgbData = [];

% Loop through each image in the folder
for i = 1:length(fileList)
    % Read the image
    img = imread(fullfile(folder, fileList(i).name));
    
    % Extract RGB values from the image
    % Reshape the image into a 2D matrix (rows x columns x 3) for RGB values
    imgRGB = reshape(img, [], 3);
    
    % Append the RGB values to rgbData
    rgbData = [rgbData; imgRGB];
end

% Write RGB values to an Excel sheet
filename = 'rgb_dataset.xlsx';
xlswrite(filename, rgbData, 'Sheet1');

disp('RGB values extracted and stored in Excel sheet.');
