---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: FD2E3442-9CEA-4390-BE9C-772C7D6FD1E2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/remove-azurermbatchapplicationpackage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureRmBatchApplicationPackage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureRmBatchApplicationPackage.md
ms.openlocfilehash: 7d8552ccc2c293f33c71402043a28bfad32ceeeb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93445711"
---
# <span data-ttu-id="8ff9b-101">Remove-AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="8ff9b-101">Remove-AzureRmBatchApplicationPackage</span></span>

## <span data-ttu-id="8ff9b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8ff9b-102">SYNOPSIS</span></span>
<span data-ttu-id="8ff9b-103">刪除應用程式套件記錄和二進位檔案。</span><span class="sxs-lookup"><span data-stu-id="8ff9b-103">Deletes an application package record and the binary file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8ff9b-104">句法</span><span class="sxs-lookup"><span data-stu-id="8ff9b-104">SYNTAX</span></span>

```
Remove-AzureRmBatchApplicationPackage [-AccountName] <String> [-ResourceGroupName] <String>
 [-ApplicationId] <String> [-ApplicationVersion] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8ff9b-105">說明</span><span class="sxs-lookup"><span data-stu-id="8ff9b-105">DESCRIPTION</span></span>
<span data-ttu-id="8ff9b-106">**AzureRmBatchApplicationPackage** Cmdlet 會從 Azure Batch 帳戶刪除應用程式套件記錄和二進位檔案。</span><span class="sxs-lookup"><span data-stu-id="8ff9b-106">The **Remove-AzureRmBatchApplicationPackage** cmdlet deletes an application package record and the binary file from an Azure Batch account.</span></span>

## <span data-ttu-id="8ff9b-107">示例</span><span class="sxs-lookup"><span data-stu-id="8ff9b-107">EXAMPLES</span></span>

### <span data-ttu-id="8ff9b-108">範例1：從 Batch 帳戶刪除應用程式套件</span><span class="sxs-lookup"><span data-stu-id="8ff9b-108">Example 1: Delete an application package from a Batch account</span></span>
```
PS C:\>Remove-AzureRmBatchApplicationPackage -AccountName "ContosoBatch" -ResourceGroupName "ContosoBatchGroup" -ApplicationId "litware" -ApplicationVersion "1.0"
```

<span data-ttu-id="8ff9b-109">這個命令會從 ContosoBatchGroup 帳戶刪除 Litware 應用程式的版本1.0。</span><span class="sxs-lookup"><span data-stu-id="8ff9b-109">This command deletes version 1.0 of the Litware application from the ContosoBatchGroup account.</span></span>
<span data-ttu-id="8ff9b-110">此命令會刪除套件記錄，以及包含套件二進位檔案的 blob。</span><span class="sxs-lookup"><span data-stu-id="8ff9b-110">The command deletes both the package record and the blob that contain the package binary file.</span></span>

## <span data-ttu-id="8ff9b-111">參數</span><span class="sxs-lookup"><span data-stu-id="8ff9b-111">PARAMETERS</span></span>

### <span data-ttu-id="8ff9b-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="8ff9b-112">-AccountName</span></span>
<span data-ttu-id="8ff9b-113">指定此 Cmdlet 從中刪除應用程式套件的批次帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="8ff9b-113">Specifies the name of the Batch account from which this cmdlet deletes an application package.</span></span>

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

### <span data-ttu-id="8ff9b-114">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="8ff9b-114">-ApplicationId</span></span>
<span data-ttu-id="8ff9b-115">指定應用程式的識別碼。</span><span class="sxs-lookup"><span data-stu-id="8ff9b-115">Specifies the ID of the application.</span></span>

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

### <span data-ttu-id="8ff9b-116">-ApplicationVersion</span><span class="sxs-lookup"><span data-stu-id="8ff9b-116">-ApplicationVersion</span></span>
<span data-ttu-id="8ff9b-117">指定應用程式的版本。</span><span class="sxs-lookup"><span data-stu-id="8ff9b-117">Specifies the version of the application.</span></span>

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

### <span data-ttu-id="8ff9b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8ff9b-118">-DefaultProfile</span></span>
<span data-ttu-id="8ff9b-119">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="8ff9b-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8ff9b-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8ff9b-120">-ResourceGroupName</span></span>
<span data-ttu-id="8ff9b-121">指定包含批次帳戶之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="8ff9b-121">Specifies the name of the resource group that contains the Batch account.</span></span>

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

### <span data-ttu-id="8ff9b-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ff9b-122">CommonParameters</span></span>
<span data-ttu-id="8ff9b-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8ff9b-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ff9b-124">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="8ff9b-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ff9b-125">輸入</span><span class="sxs-lookup"><span data-stu-id="8ff9b-125">INPUTS</span></span>

### <span data-ttu-id="8ff9b-126">System.object</span><span class="sxs-lookup"><span data-stu-id="8ff9b-126">System.String</span></span>

## <span data-ttu-id="8ff9b-127">輸出</span><span class="sxs-lookup"><span data-stu-id="8ff9b-127">OUTPUTS</span></span>

### <span data-ttu-id="8ff9b-128">System.void</span><span class="sxs-lookup"><span data-stu-id="8ff9b-128">System.Void</span></span>

## <span data-ttu-id="8ff9b-129">筆記</span><span class="sxs-lookup"><span data-stu-id="8ff9b-129">NOTES</span></span>

## <span data-ttu-id="8ff9b-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="8ff9b-130">RELATED LINKS</span></span>

[<span data-ttu-id="8ff9b-131">AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="8ff9b-131">Get-AzureRmBatchApplication</span></span>](./Get-AzureRmBatchApplication.md)

[<span data-ttu-id="8ff9b-132">AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="8ff9b-132">Get-AzureRmBatchApplicationPackage</span></span>](./Get-AzureRmBatchApplicationPackage.md)

[<span data-ttu-id="8ff9b-133">新-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="8ff9b-133">New-AzureRmBatchApplication</span></span>](./New-AzureRmBatchApplication.md)

[<span data-ttu-id="8ff9b-134">新-AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="8ff9b-134">New-AzureRmBatchApplicationPackage</span></span>](./New-AzureRmBatchApplicationPackage.md)

[<span data-ttu-id="8ff9b-135">移除-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="8ff9b-135">Remove-AzureRmBatchApplication</span></span>](./Remove-AzureRmBatchApplication.md)

[<span data-ttu-id="8ff9b-136">Set-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="8ff9b-136">Set-AzureRmBatchApplication</span></span>](./Set-AzureRmBatchApplication.md)


