---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 9C755BE8-0624-4CF7-AE7C-34DAF44678E8
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Disable-AzureBatchAutoScale.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Disable-AzureBatchAutoScale.md
ms.openlocfilehash: 124000fdf11b3fa5b90253fc3b9a75c040725ba8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93450872"
---
# <span data-ttu-id="2aafc-101">Disable-AzureBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="2aafc-101">Disable-AzureBatchAutoScale</span></span>

## <span data-ttu-id="2aafc-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2aafc-102">SYNOPSIS</span></span>
<span data-ttu-id="2aafc-103">停用自動縮放文件庫。</span><span class="sxs-lookup"><span data-stu-id="2aafc-103">Disables automatic scaling of a pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2aafc-104">句法</span><span class="sxs-lookup"><span data-stu-id="2aafc-104">SYNTAX</span></span>

```
Disable-AzureBatchAutoScale [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2aafc-105">說明</span><span class="sxs-lookup"><span data-stu-id="2aafc-105">DESCRIPTION</span></span>
<span data-ttu-id="2aafc-106">**Disable AzureBatchAutoScale** Cmdlet 會停用指定池的自動縮放。</span><span class="sxs-lookup"><span data-stu-id="2aafc-106">The **Disable-AzureBatchAutoScale** cmdlet disables automatic scaling of the specified pool.</span></span>

## <span data-ttu-id="2aafc-107">示例</span><span class="sxs-lookup"><span data-stu-id="2aafc-107">EXAMPLES</span></span>

### <span data-ttu-id="2aafc-108">範例1：停用自動縮放文件庫</span><span class="sxs-lookup"><span data-stu-id="2aafc-108">Example 1: Disable automatic scaling of a pool</span></span>
```
PS C:\>Disable-AzureBatchAutoScale -Id "MyPool" -BatchContext $Context
```

<span data-ttu-id="2aafc-109">這個命令會針對名為 MyPool 的池停用自動縮放。</span><span class="sxs-lookup"><span data-stu-id="2aafc-109">This command disables automatic scaling for the pool named MyPool.</span></span>

## <span data-ttu-id="2aafc-110">參數</span><span class="sxs-lookup"><span data-stu-id="2aafc-110">PARAMETERS</span></span>

### <span data-ttu-id="2aafc-111">-BatchCoNtext</span><span class="sxs-lookup"><span data-stu-id="2aafc-111">-BatchContext</span></span>
<span data-ttu-id="2aafc-112">指定此 Cmdlet 用來與批次服務互動的 **BatchAccountCoNtext** 實例。</span><span class="sxs-lookup"><span data-stu-id="2aafc-112">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="2aafc-113">若要取得包含您訂閱之便捷鍵的 **BatchAccountCoNtext** 物件，請使用 Get-AzureRmBatchAccountKeys Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="2aafc-113">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.BatchAccountContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2aafc-114">-識別碼</span><span class="sxs-lookup"><span data-stu-id="2aafc-114">-Id</span></span>
<span data-ttu-id="2aafc-115">指定該池的物件識別碼。</span><span class="sxs-lookup"><span data-stu-id="2aafc-115">Specifies the object ID of the pool.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2aafc-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2aafc-116">-DefaultProfile</span></span>
<span data-ttu-id="2aafc-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="2aafc-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2aafc-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2aafc-118">CommonParameters</span></span>
<span data-ttu-id="2aafc-119">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="2aafc-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2aafc-120">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="2aafc-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2aafc-121">輸入</span><span class="sxs-lookup"><span data-stu-id="2aafc-121">INPUTS</span></span>

### <span data-ttu-id="2aafc-122">BatchAccountCoNtext</span><span class="sxs-lookup"><span data-stu-id="2aafc-122">BatchAccountContext</span></span>
<span data-ttu-id="2aafc-123">形參 "BatchCoNtext" 接受管線中 "BatchAccountCoNtext" 類型的值</span><span class="sxs-lookup"><span data-stu-id="2aafc-123">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="2aafc-124">字串</span><span class="sxs-lookup"><span data-stu-id="2aafc-124">String</span></span>
<span data-ttu-id="2aafc-125">形參 "Id" 接受管線中類型 "String" 的值</span><span class="sxs-lookup"><span data-stu-id="2aafc-125">Parameter 'Id' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="2aafc-126">輸出</span><span class="sxs-lookup"><span data-stu-id="2aafc-126">OUTPUTS</span></span>

## <span data-ttu-id="2aafc-127">筆記</span><span class="sxs-lookup"><span data-stu-id="2aafc-127">NOTES</span></span>

## <span data-ttu-id="2aafc-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="2aafc-128">RELATED LINKS</span></span>

[<span data-ttu-id="2aafc-129">Enable-AzureBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="2aafc-129">Enable-AzureBatchAutoScale</span></span>](./Enable-AzureBatchAutoScale.md)

[<span data-ttu-id="2aafc-130">Test-AzureBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="2aafc-130">Test-AzureBatchAutoScale</span></span>](./Test-AzureBatchAutoScale.md)

[<span data-ttu-id="2aafc-131">Azure 批次 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="2aafc-131">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


