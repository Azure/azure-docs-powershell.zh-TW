---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermserviceendpointpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmServiceEndpointPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmServiceEndpointPolicy.md
ms.openlocfilehash: 657c18a02f05f2e318fe676a672e894a4aec9e50
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93453659"
---
# <span data-ttu-id="df6bb-101">New-AzureRmServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="df6bb-101">New-AzureRmServiceEndpointPolicy</span></span>

## <span data-ttu-id="df6bb-102">摘要</span><span class="sxs-lookup"><span data-stu-id="df6bb-102">SYNOPSIS</span></span>
<span data-ttu-id="df6bb-103">{{填入摘要}}</span><span class="sxs-lookup"><span data-stu-id="df6bb-103">{{Fill in the Synopsis}}</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="df6bb-104">句法</span><span class="sxs-lookup"><span data-stu-id="df6bb-104">SYNTAX</span></span>

```
New-AzureRmServiceEndpointPolicy -Name <String>
 [-ServiceEndpointDefinitions <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicyDefinition]>]
 -ResourceGroupName <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="df6bb-105">說明</span><span class="sxs-lookup"><span data-stu-id="df6bb-105">DESCRIPTION</span></span>
<span data-ttu-id="df6bb-106">**新的-AzureRmServiceEndpointPolicy** Cmdlet 會建立服務端點原則。</span><span class="sxs-lookup"><span data-stu-id="df6bb-106">The **New-AzureRmServiceEndpointPolicy** cmdlet create a service endpoint policy.</span></span>

## <span data-ttu-id="df6bb-107">示例</span><span class="sxs-lookup"><span data-stu-id="df6bb-107">EXAMPLES</span></span>

### <span data-ttu-id="df6bb-108">範例1：建立服務端點原則</span><span class="sxs-lookup"><span data-stu-id="df6bb-108">Example 1: Creates a service endpoint policy</span></span>
```
$serviceEndpointPolicy = New-AzureRmServiceEndpointPolicy -Name "Policy1" -ServiceEndpointPolicyDefinition $serviceEndpointDefinition -Location "location";
```

<span data-ttu-id="df6bb-109">這個命令會建立名為 Policy1 的服務端點原則，其中定義由 $serviceEndpointDefinition 物件定義的定義，並將其儲存在 $serviceEndpointPolicy 變數中。</span><span class="sxs-lookup"><span data-stu-id="df6bb-109">This command creates a service endpoint policy named Policy1 with definitions defined by the object $serviceEndpointDefinition and stores it in the $serviceEndpointPolicy variable.</span></span>

## <span data-ttu-id="df6bb-110">參數</span><span class="sxs-lookup"><span data-stu-id="df6bb-110">PARAMETERS</span></span>

### <span data-ttu-id="df6bb-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df6bb-111">-DefaultProfile</span></span>
<span data-ttu-id="df6bb-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="df6bb-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="df6bb-113">-Force</span><span class="sxs-lookup"><span data-stu-id="df6bb-113">-Force</span></span>
<span data-ttu-id="df6bb-114">如果您想要 overrite 資源，請不要要求確認</span><span class="sxs-lookup"><span data-stu-id="df6bb-114">Do not ask for confirmation if you want to overrite a resource</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df6bb-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="df6bb-115">-Name</span></span>
<span data-ttu-id="df6bb-116">子網的名稱</span><span class="sxs-lookup"><span data-stu-id="df6bb-116">The name of the subnet</span></span>

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

### <span data-ttu-id="df6bb-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="df6bb-117">-ResourceGroupName</span></span>
<span data-ttu-id="df6bb-118">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="df6bb-118">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="df6bb-119">-ServiceEndpointDefinitions</span><span class="sxs-lookup"><span data-stu-id="df6bb-119">-ServiceEndpointDefinitions</span></span>
<span data-ttu-id="df6bb-120">服務端點定義清單</span><span class="sxs-lookup"><span data-stu-id="df6bb-120">List of service endpoint definitions</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicyDefinition]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df6bb-121">-確認</span><span class="sxs-lookup"><span data-stu-id="df6bb-121">-Confirm</span></span>
<span data-ttu-id="df6bb-122">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="df6bb-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df6bb-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="df6bb-123">-WhatIf</span></span>
<span data-ttu-id="df6bb-124">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="df6bb-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="df6bb-125">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="df6bb-125">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df6bb-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df6bb-126">CommonParameters</span></span>
<span data-ttu-id="df6bb-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="df6bb-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="df6bb-128">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="df6bb-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df6bb-129">輸入</span><span class="sxs-lookup"><span data-stu-id="df6bb-129">INPUTS</span></span>

### <span data-ttu-id="df6bb-130">System.object</span><span class="sxs-lookup"><span data-stu-id="df6bb-130">System.String</span></span>


## <span data-ttu-id="df6bb-131">輸出</span><span class="sxs-lookup"><span data-stu-id="df6bb-131">OUTPUTS</span></span>

### <span data-ttu-id="df6bb-132">PSServiceEndpointPolicy 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="df6bb-132">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>


## <span data-ttu-id="df6bb-133">筆記</span><span class="sxs-lookup"><span data-stu-id="df6bb-133">NOTES</span></span>

## <span data-ttu-id="df6bb-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="df6bb-134">RELATED LINKS</span></span>
