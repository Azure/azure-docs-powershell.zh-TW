---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/set-azrelaynamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Set-AzRelayNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Set-AzRelayNamespace.md
ms.openlocfilehash: 6076a7fd8a71708bb3bdafdee8f1dfb0650b7088
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98274015"
---
# <span data-ttu-id="2d21b-101">Set-AzRelayNamespace</span><span class="sxs-lookup"><span data-stu-id="2d21b-101">Set-AzRelayNamespace</span></span>

## <span data-ttu-id="2d21b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2d21b-102">SYNOPSIS</span></span>
<span data-ttu-id="2d21b-103">更新現有中繼命名空間的描述。</span><span class="sxs-lookup"><span data-stu-id="2d21b-103">Updates the description of an existing Relay namespace.</span></span>

## <span data-ttu-id="2d21b-104">句法</span><span class="sxs-lookup"><span data-stu-id="2d21b-104">SYNTAX</span></span>

```
Set-AzRelayNamespace [-ResourceGroupName] <String> [-Name] <String> [-Tag <Hashtable>]
 [-InputObject <RelayNamespaceAttirbutesUpdateParameter>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2d21b-105">說明</span><span class="sxs-lookup"><span data-stu-id="2d21b-105">DESCRIPTION</span></span>
<span data-ttu-id="2d21b-106">**AzRelayNamespace** Cmdlet 會更新資源群組中指定的中繼命名空間的描述。</span><span class="sxs-lookup"><span data-stu-id="2d21b-106">The **Set-AzRelayNamespace** cmdlet updates the description of the specified Relay namespace within the resource group.</span></span>

## <span data-ttu-id="2d21b-107">示例</span><span class="sxs-lookup"><span data-stu-id="2d21b-107">EXAMPLES</span></span>

### <span data-ttu-id="2d21b-108">範例1</span><span class="sxs-lookup"><span data-stu-id="2d21b-108">Example 1</span></span>
```
PS C:\> Set-AzRelayNamespace -ResourceGroupName Default-ServiceBus-WestUS -Name TestNameSpace-Relay1 -Tag @{Tag2="Tag2Value"}

ProvisioningState  :
CreatedAt          : 4/12/2017 12:38:47 AM
UpdatedAt          : 4/12/2017 12:39:10 AM
ServiceBusEndpoint : https://TestNameSpace-Relay1.servicebus.windows.net:443/
MetricId           :
Location           :
Tags               : {[tag2, Tag2Value]}
Id                 :
Name               :
Type               :
```

<span data-ttu-id="2d21b-109">使用新的描述更新中繼命名空間。</span><span class="sxs-lookup"><span data-stu-id="2d21b-109">Updates the Relay namespace with a new description.</span></span>

## <span data-ttu-id="2d21b-110">參數</span><span class="sxs-lookup"><span data-stu-id="2d21b-110">PARAMETERS</span></span>

### <span data-ttu-id="2d21b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2d21b-111">-DefaultProfile</span></span>
<span data-ttu-id="2d21b-112">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="2d21b-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2d21b-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2d21b-113">-InputObject</span></span>
<span data-ttu-id="2d21b-114">中繼命名空間物件。</span><span class="sxs-lookup"><span data-stu-id="2d21b-114">Relay Namespace object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Relay.Models.RelayNamespaceAttirbutesUpdateParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2d21b-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="2d21b-115">-Name</span></span>
<span data-ttu-id="2d21b-116">中繼命名空間名稱。</span><span class="sxs-lookup"><span data-stu-id="2d21b-116">Relay Namespace Name.</span></span>

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

### <span data-ttu-id="2d21b-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2d21b-117">-ResourceGroupName</span></span>
<span data-ttu-id="2d21b-118">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="2d21b-118">Resource Group Name.</span></span>

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

### <span data-ttu-id="2d21b-119">-Tag</span><span class="sxs-lookup"><span data-stu-id="2d21b-119">-Tag</span></span>
<span data-ttu-id="2d21b-120">代表資源標記的 Hashtables。</span><span class="sxs-lookup"><span data-stu-id="2d21b-120">Hashtables which represents resource Tag.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2d21b-121">-確認</span><span class="sxs-lookup"><span data-stu-id="2d21b-121">-Confirm</span></span>
<span data-ttu-id="2d21b-122">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="2d21b-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d21b-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2d21b-123">-WhatIf</span></span>
<span data-ttu-id="2d21b-124">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="2d21b-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2d21b-125">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="2d21b-125">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d21b-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d21b-126">CommonParameters</span></span>
<span data-ttu-id="2d21b-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="2d21b-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d21b-128">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="2d21b-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d21b-129">輸入</span><span class="sxs-lookup"><span data-stu-id="2d21b-129">INPUTS</span></span>

### <span data-ttu-id="2d21b-130">System.object</span><span class="sxs-lookup"><span data-stu-id="2d21b-130">System.String</span></span>

### <span data-ttu-id="2d21b-131">[System.object] 集合. Hashtable</span><span class="sxs-lookup"><span data-stu-id="2d21b-131">System.Collections.Hashtable</span></span>

### <span data-ttu-id="2d21b-132">RelayNamespaceAttirbutesUpdateParameter 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="2d21b-132">Microsoft.Azure.Commands.Relay.Models.RelayNamespaceAttirbutesUpdateParameter</span></span>

## <span data-ttu-id="2d21b-133">輸出</span><span class="sxs-lookup"><span data-stu-id="2d21b-133">OUTPUTS</span></span>

### <span data-ttu-id="2d21b-134">PSRelayNamespaceAttributes 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="2d21b-134">Microsoft.Azure.Commands.Relay.Models.PSRelayNamespaceAttributes</span></span>

## <span data-ttu-id="2d21b-135">筆記</span><span class="sxs-lookup"><span data-stu-id="2d21b-135">NOTES</span></span>

## <span data-ttu-id="2d21b-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="2d21b-136">RELATED LINKS</span></span>
