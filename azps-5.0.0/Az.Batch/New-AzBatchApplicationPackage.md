---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: D53DAEB6-DC4F-473C-A193-A1E2A65326D4
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/new-azbatchapplicationpackage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchApplicationPackage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchApplicationPackage.md
ms.openlocfilehash: fc23c99cabe76834204f2fac1f3c18ae7eea1df0
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94140203"
---
# <span data-ttu-id="75e08-101">New-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="75e08-101">New-AzBatchApplicationPackage</span></span>

## <span data-ttu-id="75e08-102">摘要</span><span class="sxs-lookup"><span data-stu-id="75e08-102">SYNOPSIS</span></span>
<span data-ttu-id="75e08-103">在批次帳戶中建立應用程式套件。</span><span class="sxs-lookup"><span data-stu-id="75e08-103">Creates an application package in a Batch account.</span></span>

## <span data-ttu-id="75e08-104">句法</span><span class="sxs-lookup"><span data-stu-id="75e08-104">SYNTAX</span></span>

### <span data-ttu-id="75e08-105">UploadAndActivate (預設) </span><span class="sxs-lookup"><span data-stu-id="75e08-105">UploadAndActivate (Default)</span></span>
```
New-AzBatchApplicationPackage [-AccountName] <String> [-ResourceGroupName] <String> [-ApplicationName] <String>
 [-ApplicationVersion] <String> [-Format] <String> -FilePath <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="75e08-106">ActivateOnly</span><span class="sxs-lookup"><span data-stu-id="75e08-106">ActivateOnly</span></span>
```
New-AzBatchApplicationPackage [-AccountName] <String> [-ResourceGroupName] <String> [-ApplicationName] <String>
 [-ApplicationVersion] <String> [-Format] <String> [-ActivateOnly] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="75e08-107">說明</span><span class="sxs-lookup"><span data-stu-id="75e08-107">DESCRIPTION</span></span>
<span data-ttu-id="75e08-108">**新的-AzBatchApplicationPackage** Cmdlet 會在 Azure Batch 帳戶中建立應用程式套件。</span><span class="sxs-lookup"><span data-stu-id="75e08-108">The **New-AzBatchApplicationPackage** cmdlet creates an application package in an Azure Batch account.</span></span>

## <span data-ttu-id="75e08-109">示例</span><span class="sxs-lookup"><span data-stu-id="75e08-109">EXAMPLES</span></span>

### <span data-ttu-id="75e08-110">範例1：將應用程式套件安裝到批次帳戶</span><span class="sxs-lookup"><span data-stu-id="75e08-110">Example 1: Install an application package into a Batch account</span></span>
```
PS C:\>New-AzBatchApplicationPackage -AccountName "ContosoBatch" -ResourceGroupName "ContosoBatchGroup" -ApplicationName "Litware" -ApplicationVersion "1.0" -FilePath "litware.1.0.zip" -Format "zip"
```

<span data-ttu-id="75e08-111">這個命令會建立並啟用 Litware 應用程式的版本1.0，並將 litware.1.0.zip 內容上傳為應用程式套件內容。</span><span class="sxs-lookup"><span data-stu-id="75e08-111">This command creates and activates version 1.0 of the Litware application, and uploads the contents of litware.1.0.zip as the application package content.</span></span>

## <span data-ttu-id="75e08-112">參數</span><span class="sxs-lookup"><span data-stu-id="75e08-112">PARAMETERS</span></span>

### <span data-ttu-id="75e08-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="75e08-113">-AccountName</span></span>
<span data-ttu-id="75e08-114">指定此 Cmdlet 要新增應用程式套件之批帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="75e08-114">Specifies the name of the Batch account to which this cmdlet adds an application package.</span></span>

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

### <span data-ttu-id="75e08-115">-ActivateOnly</span><span class="sxs-lookup"><span data-stu-id="75e08-115">-ActivateOnly</span></span>
<span data-ttu-id="75e08-116">表示此 Cmdlet 會啟用已上傳的應用程式套件。</span><span class="sxs-lookup"><span data-stu-id="75e08-116">Indicates that this cmdlet activates an application package that has already been uploaded.</span></span>

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

### <span data-ttu-id="75e08-117">-ApplicationName</span><span class="sxs-lookup"><span data-stu-id="75e08-117">-ApplicationName</span></span>
<span data-ttu-id="75e08-118">指定應用程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="75e08-118">Specifies the name of the application.</span></span>

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

### <span data-ttu-id="75e08-119">-ApplicationVersion</span><span class="sxs-lookup"><span data-stu-id="75e08-119">-ApplicationVersion</span></span>
<span data-ttu-id="75e08-120">指定應用程式的版本。</span><span class="sxs-lookup"><span data-stu-id="75e08-120">Specifies the version of the application.</span></span>

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

### <span data-ttu-id="75e08-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75e08-121">-DefaultProfile</span></span>
<span data-ttu-id="75e08-122">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="75e08-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="75e08-123">-FilePath</span><span class="sxs-lookup"><span data-stu-id="75e08-123">-FilePath</span></span>
<span data-ttu-id="75e08-124">指定要上傳為應用程式套件二進位檔案的檔案。</span><span class="sxs-lookup"><span data-stu-id="75e08-124">Specifies the file to be uploaded as the application package binary file.</span></span>

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

### <span data-ttu-id="75e08-125">-Format</span><span class="sxs-lookup"><span data-stu-id="75e08-125">-Format</span></span>
<span data-ttu-id="75e08-126">指定應用程式套件二進位檔案的格式。</span><span class="sxs-lookup"><span data-stu-id="75e08-126">Specifies the format of the application package binary file.</span></span>

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

### <span data-ttu-id="75e08-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="75e08-127">-ResourceGroupName</span></span>
<span data-ttu-id="75e08-128">指定包含批次帳戶之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="75e08-128">Specifies the name of the resource group that contains the Batch account.</span></span>

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

### <span data-ttu-id="75e08-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75e08-129">CommonParameters</span></span>
<span data-ttu-id="75e08-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="75e08-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75e08-131">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="75e08-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75e08-132">輸入</span><span class="sxs-lookup"><span data-stu-id="75e08-132">INPUTS</span></span>

### <span data-ttu-id="75e08-133">System.object</span><span class="sxs-lookup"><span data-stu-id="75e08-133">System.String</span></span>

### <span data-ttu-id="75e08-134">SwitchParameter 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="75e08-134">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="75e08-135">輸出</span><span class="sxs-lookup"><span data-stu-id="75e08-135">OUTPUTS</span></span>

### <span data-ttu-id="75e08-136">Microsoft.Azure.Commands.Batch。PSApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="75e08-136">Microsoft.Azure.Commands.Batch.Models.PSApplicationPackage</span></span>

## <span data-ttu-id="75e08-137">筆記</span><span class="sxs-lookup"><span data-stu-id="75e08-137">NOTES</span></span>

## <span data-ttu-id="75e08-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="75e08-138">RELATED LINKS</span></span>

[<span data-ttu-id="75e08-139">AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="75e08-139">Get-AzBatchApplication</span></span>](./Get-AzBatchApplication.md)

[<span data-ttu-id="75e08-140">AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="75e08-140">Get-AzBatchApplicationPackage</span></span>](./Get-AzBatchApplicationPackage.md)

[<span data-ttu-id="75e08-141">新-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="75e08-141">New-AzBatchApplication</span></span>](./New-AzBatchApplication.md)

[<span data-ttu-id="75e08-142">移除-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="75e08-142">Remove-AzBatchApplication</span></span>](./Remove-AzBatchApplication.md)

[<span data-ttu-id="75e08-143">移除-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="75e08-143">Remove-AzBatchApplicationPackage</span></span>](./Remove-AzBatchApplicationPackage.md)

[<span data-ttu-id="75e08-144">Set-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="75e08-144">Set-AzBatchApplication</span></span>](./Set-AzBatchApplication.md)


