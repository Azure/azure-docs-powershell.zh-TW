---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: D53DAEB6-DC4F-473C-A193-A1E2A65326D4
online version: https://docs.microsoft.com/powershell/module/az.batch/new-azbatchapplicationpackage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchApplicationPackage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchApplicationPackage.md
ms.openlocfilehash: 766f521f5e963f05e51cd000361675a2f81bbb1e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101904145"
---
# <span data-ttu-id="53a36-101">New-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="53a36-101">New-AzBatchApplicationPackage</span></span>

## <span data-ttu-id="53a36-102">簡介</span><span class="sxs-lookup"><span data-stu-id="53a36-102">SYNOPSIS</span></span>
<span data-ttu-id="53a36-103">在批次處理帳戶中建立應用程式套件。</span><span class="sxs-lookup"><span data-stu-id="53a36-103">Creates an application package in a Batch account.</span></span>

## <span data-ttu-id="53a36-104">語法</span><span class="sxs-lookup"><span data-stu-id="53a36-104">SYNTAX</span></span>

### <span data-ttu-id="53a36-105">上傳AndActivate (預設) </span><span class="sxs-lookup"><span data-stu-id="53a36-105">UploadAndActivate (Default)</span></span>
```
New-AzBatchApplicationPackage [-AccountName] <String> [-ResourceGroupName] <String> [-ApplicationName] <String>
 [-ApplicationVersion] <String> [-Format] <String> -FilePath <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="53a36-106">ActivateOnly</span><span class="sxs-lookup"><span data-stu-id="53a36-106">ActivateOnly</span></span>
```
New-AzBatchApplicationPackage [-AccountName] <String> [-ResourceGroupName] <String> [-ApplicationName] <String>
 [-ApplicationVersion] <String> [-Format] <String> [-ActivateOnly] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="53a36-107">描述</span><span class="sxs-lookup"><span data-stu-id="53a36-107">DESCRIPTION</span></span>
<span data-ttu-id="53a36-108">**New-AzBatchApplicationPackage Cmdlet** 在 Azure Batch 帳戶中建立應用程式套件。</span><span class="sxs-lookup"><span data-stu-id="53a36-108">The **New-AzBatchApplicationPackage** cmdlet creates an application package in an Azure Batch account.</span></span>

## <span data-ttu-id="53a36-109">例子</span><span class="sxs-lookup"><span data-stu-id="53a36-109">EXAMPLES</span></span>

### <span data-ttu-id="53a36-110">範例 1：將應用程式套件安裝到 Batch 帳戶</span><span class="sxs-lookup"><span data-stu-id="53a36-110">Example 1: Install an application package into a Batch account</span></span>
```
PS C:\>New-AzBatchApplicationPackage -AccountName "ContosoBatch" -ResourceGroupName "ContosoBatchGroup" -ApplicationName "Litware" -ApplicationVersion "1.0" -FilePath "litware.1.0.zip" -Format "zip"
```

<span data-ttu-id="53a36-111">此命令會建立並啟用 Litware 應用程式的版本 1.0，並上傳 litware.1.0.zip 內容做為應用程式套件內容。</span><span class="sxs-lookup"><span data-stu-id="53a36-111">This command creates and activates version 1.0 of the Litware application, and uploads the contents of litware.1.0.zip as the application package content.</span></span>

## <span data-ttu-id="53a36-112">參數</span><span class="sxs-lookup"><span data-stu-id="53a36-112">PARAMETERS</span></span>

### <span data-ttu-id="53a36-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="53a36-113">-AccountName</span></span>
<span data-ttu-id="53a36-114">指定此 Cmdlet 新增應用程式套件的批次處理帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="53a36-114">Specifies the name of the Batch account to which this cmdlet adds an application package.</span></span>

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

### <span data-ttu-id="53a36-115">-ActivateOnly</span><span class="sxs-lookup"><span data-stu-id="53a36-115">-ActivateOnly</span></span>
<span data-ttu-id="53a36-116">表示此 Cmdlet 會啟用已上傳的應用程式套件。</span><span class="sxs-lookup"><span data-stu-id="53a36-116">Indicates that this cmdlet activates an application package that has already been uploaded.</span></span>

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

### <span data-ttu-id="53a36-117">-ApplicationName</span><span class="sxs-lookup"><span data-stu-id="53a36-117">-ApplicationName</span></span>
<span data-ttu-id="53a36-118">指定應用程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="53a36-118">Specifies the name of the application.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ApplicationId

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="53a36-119">-ApplicationVersion</span><span class="sxs-lookup"><span data-stu-id="53a36-119">-ApplicationVersion</span></span>
<span data-ttu-id="53a36-120">指定應用程式的版本。</span><span class="sxs-lookup"><span data-stu-id="53a36-120">Specifies the version of the application.</span></span>

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

### <span data-ttu-id="53a36-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53a36-121">-DefaultProfile</span></span>
<span data-ttu-id="53a36-122">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="53a36-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53a36-123">-FilePath</span><span class="sxs-lookup"><span data-stu-id="53a36-123">-FilePath</span></span>
<span data-ttu-id="53a36-124">指定要上傳為應用程式套件二進位檔案的檔案。</span><span class="sxs-lookup"><span data-stu-id="53a36-124">Specifies the file to be uploaded as the application package binary file.</span></span>

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

### <span data-ttu-id="53a36-125">-格式</span><span class="sxs-lookup"><span data-stu-id="53a36-125">-Format</span></span>
<span data-ttu-id="53a36-126">指定應用程式套件二進位檔案的格式。</span><span class="sxs-lookup"><span data-stu-id="53a36-126">Specifies the format of the application package binary file.</span></span>

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

### <span data-ttu-id="53a36-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="53a36-127">-ResourceGroupName</span></span>
<span data-ttu-id="53a36-128">指定包含批次帳戶的資源組名。</span><span class="sxs-lookup"><span data-stu-id="53a36-128">Specifies the name of the resource group that contains the Batch account.</span></span>

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

### <span data-ttu-id="53a36-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53a36-129">CommonParameters</span></span>
<span data-ttu-id="53a36-130">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="53a36-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53a36-131">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="53a36-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53a36-132">輸入</span><span class="sxs-lookup"><span data-stu-id="53a36-132">INPUTS</span></span>

### <span data-ttu-id="53a36-133">System.String</span><span class="sxs-lookup"><span data-stu-id="53a36-133">System.String</span></span>

### <span data-ttu-id="53a36-134">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="53a36-134">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="53a36-135">輸出</span><span class="sxs-lookup"><span data-stu-id="53a36-135">OUTPUTS</span></span>

### <span data-ttu-id="53a36-136">Microsoft.Azure.Commands.Batch。Models.PSApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="53a36-136">Microsoft.Azure.Commands.Batch.Models.PSApplicationPackage</span></span>

## <span data-ttu-id="53a36-137">筆記</span><span class="sxs-lookup"><span data-stu-id="53a36-137">NOTES</span></span>

## <span data-ttu-id="53a36-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="53a36-138">RELATED LINKS</span></span>

[<span data-ttu-id="53a36-139">Get-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="53a36-139">Get-AzBatchApplication</span></span>](./Get-AzBatchApplication.md)

[<span data-ttu-id="53a36-140">Get-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="53a36-140">Get-AzBatchApplicationPackage</span></span>](./Get-AzBatchApplicationPackage.md)

[<span data-ttu-id="53a36-141">New-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="53a36-141">New-AzBatchApplication</span></span>](./New-AzBatchApplication.md)

[<span data-ttu-id="53a36-142">Remove-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="53a36-142">Remove-AzBatchApplication</span></span>](./Remove-AzBatchApplication.md)

[<span data-ttu-id="53a36-143">Remove-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="53a36-143">Remove-AzBatchApplicationPackage</span></span>](./Remove-AzBatchApplicationPackage.md)

[<span data-ttu-id="53a36-144">Set-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="53a36-144">Set-AzBatchApplication</span></span>](./Set-AzBatchApplication.md)


