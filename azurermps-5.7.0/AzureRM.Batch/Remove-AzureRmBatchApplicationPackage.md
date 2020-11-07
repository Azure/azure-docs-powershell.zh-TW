---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: FD2E3442-9CEA-4390-BE9C-772C7D6FD1E2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/remove-azurermbatchapplicationpackage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureRmBatchApplicationPackage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureRmBatchApplicationPackage.md
ms.openlocfilehash: 0ae0003c4c38b7e3922694ed01f6d8f4d10a49d2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93626170"
---
# <span data-ttu-id="f30b1-101">Remove-AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="f30b1-101">Remove-AzureRmBatchApplicationPackage</span></span>

## <span data-ttu-id="f30b1-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f30b1-102">SYNOPSIS</span></span>
<span data-ttu-id="f30b1-103">刪除應用程式套件記錄和二進位檔案。</span><span class="sxs-lookup"><span data-stu-id="f30b1-103">Deletes an application package record and the binary file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f30b1-104">句法</span><span class="sxs-lookup"><span data-stu-id="f30b1-104">SYNTAX</span></span>

```
Remove-AzureRmBatchApplicationPackage [-AccountName] <String> [-ResourceGroupName] <String>
 [-ApplicationId] <String> [-ApplicationVersion] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f30b1-105">說明</span><span class="sxs-lookup"><span data-stu-id="f30b1-105">DESCRIPTION</span></span>
<span data-ttu-id="f30b1-106">**AzureRmBatchApplicationPackage** Cmdlet 會從 Azure Batch 帳戶刪除應用程式套件記錄和二進位檔案。</span><span class="sxs-lookup"><span data-stu-id="f30b1-106">The **Remove-AzureRmBatchApplicationPackage** cmdlet deletes an application package record and the binary file from an Azure Batch account.</span></span>

## <span data-ttu-id="f30b1-107">示例</span><span class="sxs-lookup"><span data-stu-id="f30b1-107">EXAMPLES</span></span>

### <span data-ttu-id="f30b1-108">範例1：從 Batch 帳戶刪除應用程式套件</span><span class="sxs-lookup"><span data-stu-id="f30b1-108">Example 1: Delete an application package from a Batch account</span></span>
```
PS C:\>Remove-AzureRmBatchApplicationPackage -AccountName "ContosoBatch" -ResourceGroupName "ContosoBatchGroup" -ApplicationId "litware" -ApplicationVersion "1.0"
```

<span data-ttu-id="f30b1-109">這個命令會從 ContosoBatchGroup 帳戶刪除 Litware 應用程式的版本1.0。</span><span class="sxs-lookup"><span data-stu-id="f30b1-109">This command deletes version 1.0 of the Litware application from the ContosoBatchGroup account.</span></span>
<span data-ttu-id="f30b1-110">此命令會刪除套件記錄，以及包含套件二進位檔案的 blob。</span><span class="sxs-lookup"><span data-stu-id="f30b1-110">The command deletes both the package record and the blob that contain the package binary file.</span></span>

## <span data-ttu-id="f30b1-111">參數</span><span class="sxs-lookup"><span data-stu-id="f30b1-111">PARAMETERS</span></span>

### <span data-ttu-id="f30b1-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="f30b1-112">-AccountName</span></span>
<span data-ttu-id="f30b1-113">指定此 Cmdlet 從中刪除應用程式套件的批次帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="f30b1-113">Specifies the name of the Batch account from which this cmdlet deletes an application package.</span></span>

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

### <span data-ttu-id="f30b1-114">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="f30b1-114">-ApplicationId</span></span>
<span data-ttu-id="f30b1-115">指定應用程式的識別碼。</span><span class="sxs-lookup"><span data-stu-id="f30b1-115">Specifies the ID of the application.</span></span>

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

### <span data-ttu-id="f30b1-116">-ApplicationVersion</span><span class="sxs-lookup"><span data-stu-id="f30b1-116">-ApplicationVersion</span></span>
<span data-ttu-id="f30b1-117">指定應用程式的版本。</span><span class="sxs-lookup"><span data-stu-id="f30b1-117">Specifies the version of the application.</span></span>

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

### <span data-ttu-id="f30b1-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f30b1-118">-DefaultProfile</span></span>
<span data-ttu-id="f30b1-119">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f30b1-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f30b1-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f30b1-120">-ResourceGroupName</span></span>
<span data-ttu-id="f30b1-121">指定包含批次帳戶之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="f30b1-121">Specifies the name of the resource group that contains the Batch account.</span></span>

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

### <span data-ttu-id="f30b1-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f30b1-122">CommonParameters</span></span>
<span data-ttu-id="f30b1-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f30b1-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f30b1-124">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="f30b1-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f30b1-125">輸入</span><span class="sxs-lookup"><span data-stu-id="f30b1-125">INPUTS</span></span>

### <span data-ttu-id="f30b1-126">所有</span><span class="sxs-lookup"><span data-stu-id="f30b1-126">None</span></span>
<span data-ttu-id="f30b1-127">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="f30b1-127">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="f30b1-128">輸出</span><span class="sxs-lookup"><span data-stu-id="f30b1-128">OUTPUTS</span></span>

## <span data-ttu-id="f30b1-129">筆記</span><span class="sxs-lookup"><span data-stu-id="f30b1-129">NOTES</span></span>

## <span data-ttu-id="f30b1-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="f30b1-130">RELATED LINKS</span></span>

[<span data-ttu-id="f30b1-131">AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="f30b1-131">Get-AzureRmBatchApplication</span></span>](./Get-AzureRmBatchApplication.md)

[<span data-ttu-id="f30b1-132">AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="f30b1-132">Get-AzureRmBatchApplicationPackage</span></span>](./Get-AzureRmBatchApplicationPackage.md)

[<span data-ttu-id="f30b1-133">新-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="f30b1-133">New-AzureRmBatchApplication</span></span>](./New-AzureRmBatchApplication.md)

[<span data-ttu-id="f30b1-134">新-AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="f30b1-134">New-AzureRmBatchApplicationPackage</span></span>](./New-AzureRmBatchApplicationPackage.md)

[<span data-ttu-id="f30b1-135">移除-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="f30b1-135">Remove-AzureRmBatchApplication</span></span>](./Remove-AzureRmBatchApplication.md)

[<span data-ttu-id="f30b1-136">Set-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="f30b1-136">Set-AzureRmBatchApplication</span></span>](./Set-AzureRmBatchApplication.md)


