---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermserviceendpointpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmServiceEndpointPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmServiceEndpointPolicyDefinition.md
ms.openlocfilehash: 12d809ad4c1df021891ab5acf384415d64aa08a3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93453651"
---
# <span data-ttu-id="1e30c-101">New-AzureRmServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="1e30c-101">New-AzureRmServiceEndpointPolicyDefinition</span></span>

## <span data-ttu-id="1e30c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1e30c-102">SYNOPSIS</span></span>
<span data-ttu-id="1e30c-103">{{填入摘要}}</span><span class="sxs-lookup"><span data-stu-id="1e30c-103">{{Fill in the Synopsis}}</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1e30c-104">句法</span><span class="sxs-lookup"><span data-stu-id="1e30c-104">SYNTAX</span></span>

```
New-AzureRmServiceEndpointPolicyDefinition -Name <String> [-Description <String>]
 [-ServiceResource <System.Collections.Generic.List`1[System.String]>] [-Service <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1e30c-105">說明</span><span class="sxs-lookup"><span data-stu-id="1e30c-105">DESCRIPTION</span></span>
<span data-ttu-id="1e30c-106">**AzureRmServiceEndpointPolicyDefinition** Cmdlet 會建立服務端點原則定義。</span><span class="sxs-lookup"><span data-stu-id="1e30c-106">The **New-AzureRmServiceEndpointPolicyDefinition** cmdlet create a service endpoint policy definition.</span></span>

## <span data-ttu-id="1e30c-107">示例</span><span class="sxs-lookup"><span data-stu-id="1e30c-107">EXAMPLES</span></span>

### <span data-ttu-id="1e30c-108">範例1：建立服務端點原則</span><span class="sxs-lookup"><span data-stu-id="1e30c-108">Example 1: Creates a service endpoint policy</span></span>
```
$policydef= New-AzureRmServiceEndpointPolicyDefinition -Name "ServiceEndpointPolicyDefinition1" -ResourceGroupName "ResourceGroup01" -Service "Microsoft.Storage" -ServiceResources "subscriptions/sub1" -Description "New Definition"
```

<span data-ttu-id="1e30c-109">這個命令會建立服務端點原則定義與 name ServiceEndpointPolicyDefinition1、service name、service 資源訂閱/sub1，以及將其儲存在 $policydef 變數中的資源群組。</span><span class="sxs-lookup"><span data-stu-id="1e30c-109">This command creates the service endpoint policy definition with name ServiceEndpointPolicyDefinition1,  service Microsoft.Storage, service resources subscriptions/sub1 and description "New Definition" that belongs to the resource group named ResourceGroup01 and stores it in the $policydef variable.</span></span>

## <span data-ttu-id="1e30c-110">參數</span><span class="sxs-lookup"><span data-stu-id="1e30c-110">PARAMETERS</span></span>

### <span data-ttu-id="1e30c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1e30c-111">-DefaultProfile</span></span>
<span data-ttu-id="1e30c-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="1e30c-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1e30c-113">-描述</span><span class="sxs-lookup"><span data-stu-id="1e30c-113">-Description</span></span>
<span data-ttu-id="1e30c-114">定義的描述</span><span class="sxs-lookup"><span data-stu-id="1e30c-114">The description of the definition</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e30c-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="1e30c-115">-Name</span></span>
<span data-ttu-id="1e30c-116">服務端點原則的名稱</span><span class="sxs-lookup"><span data-stu-id="1e30c-116">The name of the service endpoint policy</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e30c-117">-服務</span><span class="sxs-lookup"><span data-stu-id="1e30c-117">-Service</span></span>
<span data-ttu-id="1e30c-118">服務名稱</span><span class="sxs-lookup"><span data-stu-id="1e30c-118">Name of the service</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e30c-119">-ServiceResource</span><span class="sxs-lookup"><span data-stu-id="1e30c-119">-ServiceResource</span></span>
<span data-ttu-id="1e30c-120">服務資源清單</span><span class="sxs-lookup"><span data-stu-id="1e30c-120">List of service resources</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e30c-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e30c-121">CommonParameters</span></span>
<span data-ttu-id="1e30c-122">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1e30c-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="1e30c-123">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="1e30c-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e30c-124">輸入</span><span class="sxs-lookup"><span data-stu-id="1e30c-124">INPUTS</span></span>

### <span data-ttu-id="1e30c-125">所有</span><span class="sxs-lookup"><span data-stu-id="1e30c-125">None</span></span>


## <span data-ttu-id="1e30c-126">輸出</span><span class="sxs-lookup"><span data-stu-id="1e30c-126">OUTPUTS</span></span>

### <span data-ttu-id="1e30c-127">PSServiceEndpointPolicyDefinition 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="1e30c-127">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicyDefinition</span></span>


## <span data-ttu-id="1e30c-128">筆記</span><span class="sxs-lookup"><span data-stu-id="1e30c-128">NOTES</span></span>

## <span data-ttu-id="1e30c-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="1e30c-129">RELATED LINKS</span></span>
