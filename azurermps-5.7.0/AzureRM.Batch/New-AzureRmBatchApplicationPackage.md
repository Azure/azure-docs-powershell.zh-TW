---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: D53DAEB6-DC4F-473C-A193-A1E2A65326D4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/new-azurermbatchapplicationpackage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureRmBatchApplicationPackage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureRmBatchApplicationPackage.md
ms.openlocfilehash: 621aa03b2819815dc538650ea30120c63009235e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93454747"
---
# <span data-ttu-id="82b70-101">New-AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="82b70-101">New-AzureRmBatchApplicationPackage</span></span>

## <span data-ttu-id="82b70-102">摘要</span><span class="sxs-lookup"><span data-stu-id="82b70-102">SYNOPSIS</span></span>
<span data-ttu-id="82b70-103">在批次帳戶中建立應用程式套件。</span><span class="sxs-lookup"><span data-stu-id="82b70-103">Creates an application package in a Batch account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="82b70-104">句法</span><span class="sxs-lookup"><span data-stu-id="82b70-104">SYNTAX</span></span>

### <span data-ttu-id="82b70-105">UploadAndActivate (預設) </span><span class="sxs-lookup"><span data-stu-id="82b70-105">UploadAndActivate (Default)</span></span>
```
New-AzureRmBatchApplicationPackage [-AccountName] <String> [-ResourceGroupName] <String>
 [-ApplicationId] <String> [-ApplicationVersion] <String> [-Format] <String> -FilePath <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="82b70-106">ActivateOnly</span><span class="sxs-lookup"><span data-stu-id="82b70-106">ActivateOnly</span></span>
```
New-AzureRmBatchApplicationPackage [-AccountName] <String> [-ResourceGroupName] <String>
 [-ApplicationId] <String> [-ApplicationVersion] <String> [-Format] <String> [-ActivateOnly]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="82b70-107">說明</span><span class="sxs-lookup"><span data-stu-id="82b70-107">DESCRIPTION</span></span>
<span data-ttu-id="82b70-108">**新的-AzureRmBatchApplicationPackage** Cmdlet 會在 Azure Batch 帳戶中建立應用程式套件。</span><span class="sxs-lookup"><span data-stu-id="82b70-108">The **New-AzureRmBatchApplicationPackage** cmdlet creates an application package in an Azure Batch account.</span></span>

## <span data-ttu-id="82b70-109">示例</span><span class="sxs-lookup"><span data-stu-id="82b70-109">EXAMPLES</span></span>

### <span data-ttu-id="82b70-110">範例1：將應用程式套件安裝到批次帳戶</span><span class="sxs-lookup"><span data-stu-id="82b70-110">Example 1: Install an application package into a Batch account</span></span>
```
PS C:\>New-AzureRmBatchApplicationPackage -AccountName "ContosoBatch" -ResourceGroupName "ContosoBatchGroup" -ApplicationId "Litware" -ApplicationVersion "1.0" -FilePath "litware.1.0.zip" -Format "zip"
```

<span data-ttu-id="82b70-111">這個命令會建立並啟用 Litware 應用程式的版本1.0，並將 litware.1.0.zip 內容上傳為應用程式套件內容。</span><span class="sxs-lookup"><span data-stu-id="82b70-111">This command creates and activates version 1.0 of the Litware application, and uploads the contents of litware.1.0.zip as the application package content.</span></span>

## <span data-ttu-id="82b70-112">參數</span><span class="sxs-lookup"><span data-stu-id="82b70-112">PARAMETERS</span></span>

### <span data-ttu-id="82b70-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="82b70-113">-AccountName</span></span>
<span data-ttu-id="82b70-114">指定此 Cmdlet 要新增應用程式套件之批帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="82b70-114">Specifies the name of the Batch account to which this cmdlet adds an application package.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="82b70-115">-ActivateOnly</span><span class="sxs-lookup"><span data-stu-id="82b70-115">-ActivateOnly</span></span>
<span data-ttu-id="82b70-116">表示此 Cmdlet 會啟用已上傳的應用程式套件。</span><span class="sxs-lookup"><span data-stu-id="82b70-116">Indicates that this cmdlet activates an application package that has already been uploaded.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ActivateOnly
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="82b70-117">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="82b70-117">-ApplicationId</span></span>
<span data-ttu-id="82b70-118">指定應用程式的識別碼。</span><span class="sxs-lookup"><span data-stu-id="82b70-118">Specifies the ID of the application.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="82b70-119">-ApplicationVersion</span><span class="sxs-lookup"><span data-stu-id="82b70-119">-ApplicationVersion</span></span>
<span data-ttu-id="82b70-120">指定應用程式的版本。</span><span class="sxs-lookup"><span data-stu-id="82b70-120">Specifies the version of the application.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="82b70-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="82b70-121">-DefaultProfile</span></span>
<span data-ttu-id="82b70-122">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="82b70-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82b70-123">-FilePath</span><span class="sxs-lookup"><span data-stu-id="82b70-123">-FilePath</span></span>
<span data-ttu-id="82b70-124">指定要上傳為應用程式套件二進位檔案的檔案。</span><span class="sxs-lookup"><span data-stu-id="82b70-124">Specifies the file to be uploaded as the application package binary file.</span></span>

```yaml
Type: String
Parameter Sets: UploadAndActivate
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="82b70-125">-Format</span><span class="sxs-lookup"><span data-stu-id="82b70-125">-Format</span></span>
<span data-ttu-id="82b70-126">指定應用程式套件二進位檔案的格式。</span><span class="sxs-lookup"><span data-stu-id="82b70-126">Specifies the format of the application package binary file.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="82b70-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="82b70-127">-ResourceGroupName</span></span>
<span data-ttu-id="82b70-128">指定包含批次帳戶之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="82b70-128">Specifies the name of the resource group that contains the Batch account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="82b70-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82b70-129">CommonParameters</span></span>
<span data-ttu-id="82b70-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="82b70-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82b70-131">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="82b70-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82b70-132">輸入</span><span class="sxs-lookup"><span data-stu-id="82b70-132">INPUTS</span></span>

### <span data-ttu-id="82b70-133">所有</span><span class="sxs-lookup"><span data-stu-id="82b70-133">None</span></span>
<span data-ttu-id="82b70-134">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="82b70-134">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="82b70-135">輸出</span><span class="sxs-lookup"><span data-stu-id="82b70-135">OUTPUTS</span></span>

### <span data-ttu-id="82b70-136">Microsoft.Azure.Commands.Batch。PSApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="82b70-136">Microsoft.Azure.Commands.Batch.Models.PSApplicationPackage</span></span>

## <span data-ttu-id="82b70-137">筆記</span><span class="sxs-lookup"><span data-stu-id="82b70-137">NOTES</span></span>

## <span data-ttu-id="82b70-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="82b70-138">RELATED LINKS</span></span>

[<span data-ttu-id="82b70-139">AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="82b70-139">Get-AzureRmBatchApplication</span></span>](./Get-AzureRmBatchApplication.md)

[<span data-ttu-id="82b70-140">AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="82b70-140">Get-AzureRmBatchApplicationPackage</span></span>](./Get-AzureRmBatchApplicationPackage.md)

[<span data-ttu-id="82b70-141">新-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="82b70-141">New-AzureRmBatchApplication</span></span>](./New-AzureRmBatchApplication.md)

[<span data-ttu-id="82b70-142">移除-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="82b70-142">Remove-AzureRmBatchApplication</span></span>](./Remove-AzureRmBatchApplication.md)

[<span data-ttu-id="82b70-143">移除-AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="82b70-143">Remove-AzureRmBatchApplicationPackage</span></span>](./Remove-AzureRmBatchApplicationPackage.md)

[<span data-ttu-id="82b70-144">Set-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="82b70-144">Set-AzureRmBatchApplication</span></span>](./Set-AzureRmBatchApplication.md)


