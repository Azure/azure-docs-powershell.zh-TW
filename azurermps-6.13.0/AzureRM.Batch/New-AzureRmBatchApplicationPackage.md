---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: D53DAEB6-DC4F-473C-A193-A1E2A65326D4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/new-azurermbatchapplicationpackage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureRmBatchApplicationPackage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureRmBatchApplicationPackage.md
ms.openlocfilehash: bbe3dbc5a929040bfa10efac952b3500529a075d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93444000"
---
# <span data-ttu-id="415eb-101">New-AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="415eb-101">New-AzureRmBatchApplicationPackage</span></span>

## <span data-ttu-id="415eb-102">摘要</span><span class="sxs-lookup"><span data-stu-id="415eb-102">SYNOPSIS</span></span>
<span data-ttu-id="415eb-103">在批次帳戶中建立應用程式套件。</span><span class="sxs-lookup"><span data-stu-id="415eb-103">Creates an application package in a Batch account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="415eb-104">句法</span><span class="sxs-lookup"><span data-stu-id="415eb-104">SYNTAX</span></span>

### <span data-ttu-id="415eb-105">UploadAndActivate (預設) </span><span class="sxs-lookup"><span data-stu-id="415eb-105">UploadAndActivate (Default)</span></span>
```
New-AzureRmBatchApplicationPackage [-AccountName] <String> [-ResourceGroupName] <String>
 [-ApplicationId] <String> [-ApplicationVersion] <String> [-Format] <String> -FilePath <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="415eb-106">ActivateOnly</span><span class="sxs-lookup"><span data-stu-id="415eb-106">ActivateOnly</span></span>
```
New-AzureRmBatchApplicationPackage [-AccountName] <String> [-ResourceGroupName] <String>
 [-ApplicationId] <String> [-ApplicationVersion] <String> [-Format] <String> [-ActivateOnly]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="415eb-107">說明</span><span class="sxs-lookup"><span data-stu-id="415eb-107">DESCRIPTION</span></span>
<span data-ttu-id="415eb-108">**新的-AzureRmBatchApplicationPackage** Cmdlet 會在 Azure Batch 帳戶中建立應用程式套件。</span><span class="sxs-lookup"><span data-stu-id="415eb-108">The **New-AzureRmBatchApplicationPackage** cmdlet creates an application package in an Azure Batch account.</span></span>

## <span data-ttu-id="415eb-109">示例</span><span class="sxs-lookup"><span data-stu-id="415eb-109">EXAMPLES</span></span>

### <span data-ttu-id="415eb-110">範例1：將應用程式套件安裝到批次帳戶</span><span class="sxs-lookup"><span data-stu-id="415eb-110">Example 1: Install an application package into a Batch account</span></span>
```
PS C:\>New-AzureRmBatchApplicationPackage -AccountName "ContosoBatch" -ResourceGroupName "ContosoBatchGroup" -ApplicationId "Litware" -ApplicationVersion "1.0" -FilePath "litware.1.0.zip" -Format "zip"
```

<span data-ttu-id="415eb-111">這個命令會建立並啟用 Litware 應用程式的版本1.0，並將 litware.1.0.zip 內容上傳為應用程式套件內容。</span><span class="sxs-lookup"><span data-stu-id="415eb-111">This command creates and activates version 1.0 of the Litware application, and uploads the contents of litware.1.0.zip as the application package content.</span></span>

## <span data-ttu-id="415eb-112">參數</span><span class="sxs-lookup"><span data-stu-id="415eb-112">PARAMETERS</span></span>

### <span data-ttu-id="415eb-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="415eb-113">-AccountName</span></span>
<span data-ttu-id="415eb-114">指定此 Cmdlet 要新增應用程式套件之批帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="415eb-114">Specifies the name of the Batch account to which this cmdlet adds an application package.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="415eb-115">-ActivateOnly</span><span class="sxs-lookup"><span data-stu-id="415eb-115">-ActivateOnly</span></span>
<span data-ttu-id="415eb-116">表示此 Cmdlet 會啟用已上傳的應用程式套件。</span><span class="sxs-lookup"><span data-stu-id="415eb-116">Indicates that this cmdlet activates an application package that has already been uploaded.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ActivateOnly
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="415eb-117">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="415eb-117">-ApplicationId</span></span>
<span data-ttu-id="415eb-118">指定應用程式的識別碼。</span><span class="sxs-lookup"><span data-stu-id="415eb-118">Specifies the ID of the application.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="415eb-119">-ApplicationVersion</span><span class="sxs-lookup"><span data-stu-id="415eb-119">-ApplicationVersion</span></span>
<span data-ttu-id="415eb-120">指定應用程式的版本。</span><span class="sxs-lookup"><span data-stu-id="415eb-120">Specifies the version of the application.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="415eb-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="415eb-121">-DefaultProfile</span></span>
<span data-ttu-id="415eb-122">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="415eb-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="415eb-123">-FilePath</span><span class="sxs-lookup"><span data-stu-id="415eb-123">-FilePath</span></span>
<span data-ttu-id="415eb-124">指定要上傳為應用程式套件二進位檔案的檔案。</span><span class="sxs-lookup"><span data-stu-id="415eb-124">Specifies the file to be uploaded as the application package binary file.</span></span>

```yaml
Type: System.String
Parameter Sets: UploadAndActivate
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="415eb-125">-Format</span><span class="sxs-lookup"><span data-stu-id="415eb-125">-Format</span></span>
<span data-ttu-id="415eb-126">指定應用程式套件二進位檔案的格式。</span><span class="sxs-lookup"><span data-stu-id="415eb-126">Specifies the format of the application package binary file.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="415eb-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="415eb-127">-ResourceGroupName</span></span>
<span data-ttu-id="415eb-128">指定包含批次帳戶之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="415eb-128">Specifies the name of the resource group that contains the Batch account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="415eb-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="415eb-129">CommonParameters</span></span>
<span data-ttu-id="415eb-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="415eb-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="415eb-131">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="415eb-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="415eb-132">輸入</span><span class="sxs-lookup"><span data-stu-id="415eb-132">INPUTS</span></span>

### <span data-ttu-id="415eb-133">System.object</span><span class="sxs-lookup"><span data-stu-id="415eb-133">System.String</span></span>

### <span data-ttu-id="415eb-134">SwitchParameter 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="415eb-134">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="415eb-135">輸出</span><span class="sxs-lookup"><span data-stu-id="415eb-135">OUTPUTS</span></span>

### <span data-ttu-id="415eb-136">Microsoft.Azure.Commands.Batch。PSApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="415eb-136">Microsoft.Azure.Commands.Batch.Models.PSApplicationPackage</span></span>

## <span data-ttu-id="415eb-137">筆記</span><span class="sxs-lookup"><span data-stu-id="415eb-137">NOTES</span></span>

## <span data-ttu-id="415eb-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="415eb-138">RELATED LINKS</span></span>

[<span data-ttu-id="415eb-139">AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="415eb-139">Get-AzureRmBatchApplication</span></span>](./Get-AzureRmBatchApplication.md)

[<span data-ttu-id="415eb-140">AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="415eb-140">Get-AzureRmBatchApplicationPackage</span></span>](./Get-AzureRmBatchApplicationPackage.md)

[<span data-ttu-id="415eb-141">新-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="415eb-141">New-AzureRmBatchApplication</span></span>](./New-AzureRmBatchApplication.md)

[<span data-ttu-id="415eb-142">移除-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="415eb-142">Remove-AzureRmBatchApplication</span></span>](./Remove-AzureRmBatchApplication.md)

[<span data-ttu-id="415eb-143">移除-AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="415eb-143">Remove-AzureRmBatchApplicationPackage</span></span>](./Remove-AzureRmBatchApplicationPackage.md)

[<span data-ttu-id="415eb-144">Set-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="415eb-144">Set-AzureRmBatchApplication</span></span>](./Set-AzureRmBatchApplication.md)


