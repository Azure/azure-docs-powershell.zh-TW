---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermserviceendpointpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmServiceEndpointPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmServiceEndpointPolicyDefinition.md
ms.openlocfilehash: ac58450295e0e2d988c12c308c0210b38ad71b4c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93625275"
---
# <span data-ttu-id="e7ae6-101">Add-AzureRmServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="e7ae6-101">Add-AzureRmServiceEndpointPolicyDefinition</span></span>

## <span data-ttu-id="e7ae6-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e7ae6-102">SYNOPSIS</span></span>
<span data-ttu-id="e7ae6-103">將服務端點原則定義新增到指定的原則。</span><span class="sxs-lookup"><span data-stu-id="e7ae6-103">Adds a service endpoint policy definition to a specified policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e7ae6-104">句法</span><span class="sxs-lookup"><span data-stu-id="e7ae6-104">SYNTAX</span></span>

```
Add-AzureRmServiceEndpointPolicyDefinition -Name <String> -ServiceEndpointPolicy <PSServiceEndpointPolicy>
 [-Description <String>] [-ServiceResource <System.Collections.Generic.List`1[System.String]>]
 [-Service <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e7ae6-105">說明</span><span class="sxs-lookup"><span data-stu-id="e7ae6-105">DESCRIPTION</span></span>
<span data-ttu-id="e7ae6-106">**AzureRmServiceEndpointPolicyDefinition** Cmdlet 會將服務端點原則定義新增至原則。</span><span class="sxs-lookup"><span data-stu-id="e7ae6-106">The **Add-AzureRmServiceEndpointPolicyDefinition** cmdlet add a service endpoint policy definition to the policy.</span></span>

## <span data-ttu-id="e7ae6-107">示例</span><span class="sxs-lookup"><span data-stu-id="e7ae6-107">EXAMPLES</span></span>

### <span data-ttu-id="e7ae6-108">範例1：更新服務端點原則中的服務端點原則定義</span><span class="sxs-lookup"><span data-stu-id="e7ae6-108">Example 1: Updates a service endpoint policy definition in a service endpoint policy</span></span>
```
$policydef= New-AzureRmServiceEndpointPolicyDefinition -Name "ServiceEndpointPolicyDefinition1" -ResourceGroupName "ResourceGroup01" -Service "Microsoft.Storage" -ServiceResources "subscriptions/sub1" -Description "New Definition"
```

<span data-ttu-id="e7ae6-109">這個命令會更新服務端點原則定義與 name ServiceEndpointPolicyDefinition1、service name、service 資源訂閱/sub1，以及將其儲存在 $policydef 變數中的資源群組。</span><span class="sxs-lookup"><span data-stu-id="e7ae6-109">This command updated the service endpoint policy definition with name ServiceEndpointPolicyDefinition1,  service Microsoft.Storage, service resources subscriptions/sub1 and description "New Definition" that belongs to the resource group named ResourceGroup01 and stores it in the $policydef variable.</span></span>

## <span data-ttu-id="e7ae6-110">參數</span><span class="sxs-lookup"><span data-stu-id="e7ae6-110">PARAMETERS</span></span>

### <span data-ttu-id="e7ae6-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7ae6-111">-DefaultProfile</span></span>
<span data-ttu-id="e7ae6-112">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e7ae6-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e7ae6-113">-描述</span><span class="sxs-lookup"><span data-stu-id="e7ae6-113">-Description</span></span>
<span data-ttu-id="e7ae6-114">定義的描述</span><span class="sxs-lookup"><span data-stu-id="e7ae6-114">The description of the definition</span></span>

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

### <span data-ttu-id="e7ae6-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="e7ae6-115">-Name</span></span>
<span data-ttu-id="e7ae6-116">服務端點原則定義的名稱</span><span class="sxs-lookup"><span data-stu-id="e7ae6-116">The name of the service endpoint policy definition</span></span>

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

### <span data-ttu-id="e7ae6-117">-服務</span><span class="sxs-lookup"><span data-stu-id="e7ae6-117">-Service</span></span>
<span data-ttu-id="e7ae6-118">服務名稱</span><span class="sxs-lookup"><span data-stu-id="e7ae6-118">Name of the service</span></span>

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

### <span data-ttu-id="e7ae6-119">-ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="e7ae6-119">-ServiceEndpointPolicy</span></span>
<span data-ttu-id="e7ae6-120">ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="e7ae6-120">The ServiceEndpointPolicy</span></span>

```yaml
Type: PSServiceEndpointPolicy
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e7ae6-121">-ServiceResource</span><span class="sxs-lookup"><span data-stu-id="e7ae6-121">-ServiceResource</span></span>
<span data-ttu-id="e7ae6-122">服務資源清單</span><span class="sxs-lookup"><span data-stu-id="e7ae6-122">List of service resources</span></span>

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

### <span data-ttu-id="e7ae6-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7ae6-123">CommonParameters</span></span>
<span data-ttu-id="e7ae6-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e7ae6-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="e7ae6-125">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="e7ae6-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7ae6-126">輸入</span><span class="sxs-lookup"><span data-stu-id="e7ae6-126">INPUTS</span></span>

### <span data-ttu-id="e7ae6-127">PSServiceEndpointPolicy 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="e7ae6-127">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>


## <span data-ttu-id="e7ae6-128">輸出</span><span class="sxs-lookup"><span data-stu-id="e7ae6-128">OUTPUTS</span></span>

### <span data-ttu-id="e7ae6-129">PSServiceEndpointPolicy 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="e7ae6-129">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>


## <span data-ttu-id="e7ae6-130">筆記</span><span class="sxs-lookup"><span data-stu-id="e7ae6-130">NOTES</span></span>

## <span data-ttu-id="e7ae6-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="e7ae6-131">RELATED LINKS</span></span>
