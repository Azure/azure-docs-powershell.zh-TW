---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: AFDE5ECD-29AB-4C91-98BF-1B8C9C3BB079
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureRmBatchAccountKeys.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureRmBatchAccountKeys.md
ms.openlocfilehash: 6bab9613a2b109ef0cd8d0d65bf2fb770d91eb16
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93625528"
---
# <span data-ttu-id="16bfb-101">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="16bfb-101">Get-AzureRmBatchAccountKeys</span></span>

## <span data-ttu-id="16bfb-102">摘要</span><span class="sxs-lookup"><span data-stu-id="16bfb-102">SYNOPSIS</span></span>
<span data-ttu-id="16bfb-103">取得批次帳戶的金鑰。</span><span class="sxs-lookup"><span data-stu-id="16bfb-103">Gets the keys of a Batch account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="16bfb-104">句法</span><span class="sxs-lookup"><span data-stu-id="16bfb-104">SYNTAX</span></span>

```
Get-AzureRmBatchAccountKeys [-AccountName] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="16bfb-105">說明</span><span class="sxs-lookup"><span data-stu-id="16bfb-105">DESCRIPTION</span></span>
<span data-ttu-id="16bfb-106">**AzureRmBatchAccountKeys** Cmdlet 會在目前的訂閱中取得 Azure Batch 帳戶的金鑰。</span><span class="sxs-lookup"><span data-stu-id="16bfb-106">The **Get-AzureRmBatchAccountKeys** cmdlet gets the keys of an Azure Batch account in the current subscription.</span></span>

## <span data-ttu-id="16bfb-107">示例</span><span class="sxs-lookup"><span data-stu-id="16bfb-107">EXAMPLES</span></span>

## <span data-ttu-id="16bfb-108">參數</span><span class="sxs-lookup"><span data-stu-id="16bfb-108">PARAMETERS</span></span>

### <span data-ttu-id="16bfb-109">-AccountName</span><span class="sxs-lookup"><span data-stu-id="16bfb-109">-AccountName</span></span>
<span data-ttu-id="16bfb-110">指定此 Cmdlet 取得金鑰的帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="16bfb-110">Specifies the name of the account for which this cmdlet gets keys.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="16bfb-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="16bfb-111">-ResourceGroupName</span></span>
<span data-ttu-id="16bfb-112">指定包含此 Cmdlet 取得金鑰之帳戶的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="16bfb-112">Specifies the name of the resource group that contains the account for which this cmdlet gets keys.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="16bfb-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16bfb-113">-DefaultProfile</span></span>
<span data-ttu-id="16bfb-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="16bfb-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="16bfb-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16bfb-115">CommonParameters</span></span>
<span data-ttu-id="16bfb-116">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="16bfb-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16bfb-117">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="16bfb-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16bfb-118">輸入</span><span class="sxs-lookup"><span data-stu-id="16bfb-118">INPUTS</span></span>

## <span data-ttu-id="16bfb-119">輸出</span><span class="sxs-lookup"><span data-stu-id="16bfb-119">OUTPUTS</span></span>

### <span data-ttu-id="16bfb-120">Microsoft.Azure.Commands.Batch.BatchAccountCoNtext</span><span class="sxs-lookup"><span data-stu-id="16bfb-120">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="16bfb-121">筆記</span><span class="sxs-lookup"><span data-stu-id="16bfb-121">NOTES</span></span>

## <span data-ttu-id="16bfb-122">相關連結</span><span class="sxs-lookup"><span data-stu-id="16bfb-122">RELATED LINKS</span></span>

[<span data-ttu-id="16bfb-123">新-AzureRmBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="16bfb-123">New-AzureRmBatchAccountKey</span></span>](./New-AzureRmBatchAccountKey.md)

[<span data-ttu-id="16bfb-124">Azure 批次 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="16bfb-124">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


