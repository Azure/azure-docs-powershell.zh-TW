---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 486748AC-3932-4E0C-BBCC-2BC194E69DCC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/new-azurermbatchaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureRmBatchAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureRmBatchAccountKey.md
ms.openlocfilehash: 48de3ae521f77c531433ffca67dadc9e2c46a980
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93453876"
---
# <span data-ttu-id="33c49-101">New-AzureRmBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="33c49-101">New-AzureRmBatchAccountKey</span></span>

## <span data-ttu-id="33c49-102">摘要</span><span class="sxs-lookup"><span data-stu-id="33c49-102">SYNOPSIS</span></span>
<span data-ttu-id="33c49-103">再生批次帳戶的金鑰。</span><span class="sxs-lookup"><span data-stu-id="33c49-103">Regenerates a key of a Batch account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="33c49-104">句法</span><span class="sxs-lookup"><span data-stu-id="33c49-104">SYNTAX</span></span>

```
New-AzureRmBatchAccountKey [-AccountName] <String> [-ResourceGroupName <String>] -KeyType <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="33c49-105">說明</span><span class="sxs-lookup"><span data-stu-id="33c49-105">DESCRIPTION</span></span>
<span data-ttu-id="33c49-106">**新的-AzureRmBatchAccountKey** Cmdlet 會重新產生 Azure Batch 帳戶的主要或次要金鑰。</span><span class="sxs-lookup"><span data-stu-id="33c49-106">The **New-AzureRmBatchAccountKey** cmdlet regenerates the primary or secondary key of an Azure Batch account.</span></span>
<span data-ttu-id="33c49-107">Cmdlet 會傳回 **BatchAccountCoNtext** 物件，該物件具有其目前的 **PrimaryAccountKey** 和 **SecondaryAccountKey** 屬性。</span><span class="sxs-lookup"><span data-stu-id="33c49-107">The cmdlet returns a **BatchAccountContext** object that has its current **PrimaryAccountKey** and **SecondaryAccountKey** properties.</span></span>

## <span data-ttu-id="33c49-108">示例</span><span class="sxs-lookup"><span data-stu-id="33c49-108">EXAMPLES</span></span>

### <span data-ttu-id="33c49-109">範例1：在批次帳戶上重新產生主要帳戶金鑰</span><span class="sxs-lookup"><span data-stu-id="33c49-109">Example 1: Regenerate the primary account key on a Batch account</span></span>
```
PS C:\>New-AzureRmBatchAccountKey -AccountName "pfuller" -KeyType "Primary"
AccountName                  : pfuller

Location                     : westus

ResourceGroupName            : CmdletExampleRG

CoreQuota                    : 20

PoolQuota                    : 20

ActiveJobAndJobScheduleQuota : 20

Tags                         : 
TaskTenantUrl                : https://cmdletexample.westus.batch.azure.com
```

<span data-ttu-id="33c49-110">這個命令會在名為 pfuller 的批次帳戶上，重新生成主要帳戶金鑰。</span><span class="sxs-lookup"><span data-stu-id="33c49-110">This command regenerates the primary account key on the Batch account named pfuller.</span></span>

## <span data-ttu-id="33c49-111">參數</span><span class="sxs-lookup"><span data-stu-id="33c49-111">PARAMETERS</span></span>

### <span data-ttu-id="33c49-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="33c49-112">-AccountName</span></span>
<span data-ttu-id="33c49-113">指定此 Cmdlet 為其重新生成金鑰的批次帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="33c49-113">Specifies the name of the Batch account for which this cmdlet regenerates a key.</span></span>

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

### <span data-ttu-id="33c49-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="33c49-114">-DefaultProfile</span></span>
<span data-ttu-id="33c49-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="33c49-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="33c49-116">-KeyType</span><span class="sxs-lookup"><span data-stu-id="33c49-116">-KeyType</span></span>
<span data-ttu-id="33c49-117">指定此 Cmdlet 所再生的金鑰類型。</span><span class="sxs-lookup"><span data-stu-id="33c49-117">Specifies the type of key that this cmdlet regenerates.</span></span>
<span data-ttu-id="33c49-118">有效值為：</span><span class="sxs-lookup"><span data-stu-id="33c49-118">Valid values are:</span></span> 
- <span data-ttu-id="33c49-119">首選</span><span class="sxs-lookup"><span data-stu-id="33c49-119">Primary</span></span>
- <span data-ttu-id="33c49-120">備用</span><span class="sxs-lookup"><span data-stu-id="33c49-120">Secondary</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Primary, Secondary

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33c49-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="33c49-121">-ResourceGroupName</span></span>
<span data-ttu-id="33c49-122">指定此 Cmdlet 為其重新生成金鑰的帳戶資源群組。</span><span class="sxs-lookup"><span data-stu-id="33c49-122">Specifies the resource group of the account for which this cmdlet regenerates a key.</span></span>

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

### <span data-ttu-id="33c49-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="33c49-123">CommonParameters</span></span>
<span data-ttu-id="33c49-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="33c49-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="33c49-125">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="33c49-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="33c49-126">輸入</span><span class="sxs-lookup"><span data-stu-id="33c49-126">INPUTS</span></span>

### <span data-ttu-id="33c49-127">System.object</span><span class="sxs-lookup"><span data-stu-id="33c49-127">System.String</span></span>

## <span data-ttu-id="33c49-128">輸出</span><span class="sxs-lookup"><span data-stu-id="33c49-128">OUTPUTS</span></span>

### <span data-ttu-id="33c49-129">Microsoft.Azure.Commands.Batch.BatchAccountCoNtext</span><span class="sxs-lookup"><span data-stu-id="33c49-129">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="33c49-130">筆記</span><span class="sxs-lookup"><span data-stu-id="33c49-130">NOTES</span></span>

## <span data-ttu-id="33c49-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="33c49-131">RELATED LINKS</span></span>

[<span data-ttu-id="33c49-132">AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="33c49-132">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="33c49-133">Azure 批次 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="33c49-133">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


