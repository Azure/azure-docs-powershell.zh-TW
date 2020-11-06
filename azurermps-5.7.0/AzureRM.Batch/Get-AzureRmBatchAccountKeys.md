---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: AFDE5ECD-29AB-4C91-98BF-1B8C9C3BB079
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/get-azurermbatchaccountkeys
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureRmBatchAccountKeys.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureRmBatchAccountKeys.md
ms.openlocfilehash: 8e6e10c45034402e5339ed5cb6d60a9319362450
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93444772"
---
# <span data-ttu-id="56206-101">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="56206-101">Get-AzureRmBatchAccountKeys</span></span>

## <span data-ttu-id="56206-102">摘要</span><span class="sxs-lookup"><span data-stu-id="56206-102">SYNOPSIS</span></span>
<span data-ttu-id="56206-103">取得批次帳戶的金鑰。</span><span class="sxs-lookup"><span data-stu-id="56206-103">Gets the keys of a Batch account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="56206-104">句法</span><span class="sxs-lookup"><span data-stu-id="56206-104">SYNTAX</span></span>

```
Get-AzureRmBatchAccountKeys [-AccountName] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="56206-105">說明</span><span class="sxs-lookup"><span data-stu-id="56206-105">DESCRIPTION</span></span>
<span data-ttu-id="56206-106">**AzureRmBatchAccountKeys** Cmdlet 會在目前的訂閱中取得 Azure Batch 帳戶的金鑰。</span><span class="sxs-lookup"><span data-stu-id="56206-106">The **Get-AzureRmBatchAccountKeys** cmdlet gets the keys of an Azure Batch account in the current subscription.</span></span>

## <span data-ttu-id="56206-107">示例</span><span class="sxs-lookup"><span data-stu-id="56206-107">EXAMPLES</span></span>

## <span data-ttu-id="56206-108">參數</span><span class="sxs-lookup"><span data-stu-id="56206-108">PARAMETERS</span></span>

### <span data-ttu-id="56206-109">-AccountName</span><span class="sxs-lookup"><span data-stu-id="56206-109">-AccountName</span></span>
<span data-ttu-id="56206-110">指定此 Cmdlet 取得金鑰的帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="56206-110">Specifies the name of the account for which this cmdlet gets keys.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="56206-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56206-111">-DefaultProfile</span></span>
<span data-ttu-id="56206-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="56206-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="56206-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="56206-113">-ResourceGroupName</span></span>
<span data-ttu-id="56206-114">指定包含此 Cmdlet 取得金鑰之帳戶的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="56206-114">Specifies the name of the resource group that contains the account for which this cmdlet gets keys.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="56206-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56206-115">CommonParameters</span></span>
<span data-ttu-id="56206-116">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="56206-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56206-117">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="56206-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56206-118">輸入</span><span class="sxs-lookup"><span data-stu-id="56206-118">INPUTS</span></span>

### <span data-ttu-id="56206-119">所有</span><span class="sxs-lookup"><span data-stu-id="56206-119">None</span></span>
<span data-ttu-id="56206-120">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="56206-120">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="56206-121">輸出</span><span class="sxs-lookup"><span data-stu-id="56206-121">OUTPUTS</span></span>

### <span data-ttu-id="56206-122">Microsoft.Azure.Commands.Batch.BatchAccountCoNtext</span><span class="sxs-lookup"><span data-stu-id="56206-122">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="56206-123">筆記</span><span class="sxs-lookup"><span data-stu-id="56206-123">NOTES</span></span>

## <span data-ttu-id="56206-124">相關連結</span><span class="sxs-lookup"><span data-stu-id="56206-124">RELATED LINKS</span></span>

[<span data-ttu-id="56206-125">新-AzureRmBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="56206-125">New-AzureRmBatchAccountKey</span></span>](./New-AzureRmBatchAccountKey.md)

[<span data-ttu-id="56206-126">Azure 批次 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="56206-126">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


