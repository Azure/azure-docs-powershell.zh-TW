---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/set-azwcfrelay
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Set-AzWcfRelay.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Set-AzWcfRelay.md
ms.openlocfilehash: 04925f904861eea006c6480dbdb48794afc55c56
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93792261"
---
# <span data-ttu-id="85ae4-101">Set-AzWcfRelay</span><span class="sxs-lookup"><span data-stu-id="85ae4-101">Set-AzWcfRelay</span></span>

## <span data-ttu-id="85ae4-102">摘要</span><span class="sxs-lookup"><span data-stu-id="85ae4-102">SYNOPSIS</span></span>
<span data-ttu-id="85ae4-103">更新指定的中繼命名空間中 WcfRelay 的描述。</span><span class="sxs-lookup"><span data-stu-id="85ae4-103">Updates the description of a WcfRelay in the specified Relay namespace.</span></span>

## <span data-ttu-id="85ae4-104">句法</span><span class="sxs-lookup"><span data-stu-id="85ae4-104">SYNTAX</span></span>

### <span data-ttu-id="85ae4-105">WcfRelayInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="85ae4-105">WcfRelayInputObjectSet</span></span>
```
Set-AzWcfRelay [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-InputObject <PSWcfRelayAttributes>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="85ae4-106">WcfRelayPropertiesSet</span><span class="sxs-lookup"><span data-stu-id="85ae4-106">WcfRelayPropertiesSet</span></span>
```
Set-AzWcfRelay [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String> [-UserMetadata <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="85ae4-107">說明</span><span class="sxs-lookup"><span data-stu-id="85ae4-107">DESCRIPTION</span></span>
<span data-ttu-id="85ae4-108">Set-AzWcfRelay Cmdlet 會更新指定的中繼命名空間中 WcfRelay 的描述。</span><span class="sxs-lookup"><span data-stu-id="85ae4-108">The Set-AzWcfRelay cmdlet updates the description for the WcfRelay in the specified Relay namespace.</span></span>

## <span data-ttu-id="85ae4-109">示例</span><span class="sxs-lookup"><span data-stu-id="85ae4-109">EXAMPLES</span></span>

### <span data-ttu-id="85ae4-110">範例 1-InputObject</span><span class="sxs-lookup"><span data-stu-id="85ae4-110">Example 1 - InputObject</span></span>
```
PS C:\>
PS C:\> $getWcfRelay = Get-AzWcfRelay -ResourceGroupName Default-ServiceBus-WestUS -NamespaceName TestNameSpace-Relay1 -WcfRelayName TestWCFRelay
PS C:\> $getWcfRelay.UserMetadata = "usermetadata is a placeholder to store user-defined string data for the HybridConnection endpoint.e.g. it can be used to store  desc
riptive data, such as list of teams and their contact information also user-defined configuration settings can be stored."
PS C:\> Set-AzWcfRelay -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name TestWCFRelay1 -InputObject $getWcfRelay

RelayType                   : Http
CreatedAt                   : 4/26/2017 5:14:46 PM
UpdatedAt                   : 4/26/2017 5:16:50 PM
ListenerCount               :
RequiresClientAuthorization : False
RequiresTransportSecurity   : True
IsDynamic                   : False
UserMetadata                : usermetadata is a placeholder to store user-defined string data for the HybridConnection endpoint.e.g. it can be used to store  desc
riptive data, such as list of teams and their contact information also user-defined configuration settings can be stored.
Id                          : /subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/Default-Storage-WestUS/providers/Microsoft.Rel
                              ay/namespaces/TestNameSpace-Relay1/WcfRelays/TestWCFRelay2
Name                        : TestWCFRelay2
Type                        : Microsoft.Relay/WcfRelays
```

### <span data-ttu-id="85ae4-111">範例 2-屬性</span><span class="sxs-lookup"><span data-stu-id="85ae4-111">Example 2 - Properties</span></span>
```
PS C:\> Set-AzWcfRelay -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name TestWCFRelay1 -UserMetadata "User Meta data"

RelayType                   : NetTcp
CreatedAt                   : 4/26/2017 5:20:08 PM
UpdatedAt                   : 4/26/2017 5:26:09 PM
ListenerCount               :
RequiresClientAuthorization : True
RequiresTransportSecurity   : True
IsDynamic                   : False
UserMetadata                : User Meta data
Id                          : /subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/Default-Storage-WestUS/providers/Microsoft.Rel
                              ay/namespaces/TestNameSpace-Relay1/WcfRelays/TestWCFRelay
Name                        : TestWCFRelay
Type                        : Microsoft.Relay/WcfRelays
```

<span data-ttu-id="85ae4-112">使用指定命名空間中的新描述更新指定的 WcfRelay。</span><span class="sxs-lookup"><span data-stu-id="85ae4-112">Updates the specified WcfRelay with a new description in the specified namespace.</span></span>
<span data-ttu-id="85ae4-113">這個範例會使用新的值更新 UserMetadata 屬性。</span><span class="sxs-lookup"><span data-stu-id="85ae4-113">This example updates the UserMetadata property with new value.</span></span>

## <span data-ttu-id="85ae4-114">參數</span><span class="sxs-lookup"><span data-stu-id="85ae4-114">PARAMETERS</span></span>

### <span data-ttu-id="85ae4-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="85ae4-115">-DefaultProfile</span></span>
<span data-ttu-id="85ae4-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="85ae4-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="85ae4-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="85ae4-117">-InputObject</span></span>
<span data-ttu-id="85ae4-118">WcfRelay 物件。</span><span class="sxs-lookup"><span data-stu-id="85ae4-118">WcfRelay object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Relay.Models.PSWcfRelayAttributes
Parameter Sets: WcfRelayInputObjectSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="85ae4-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="85ae4-119">-Name</span></span>
<span data-ttu-id="85ae4-120">WcfRelay [名稱]。</span><span class="sxs-lookup"><span data-stu-id="85ae4-120">WcfRelay Name.</span></span>

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

### <span data-ttu-id="85ae4-121">-命名空間</span><span class="sxs-lookup"><span data-stu-id="85ae4-121">-Namespace</span></span>
<span data-ttu-id="85ae4-122">命名空間名稱。</span><span class="sxs-lookup"><span data-stu-id="85ae4-122">Namespace Name.</span></span>

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

### <span data-ttu-id="85ae4-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="85ae4-123">-ResourceGroupName</span></span>
<span data-ttu-id="85ae4-124">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="85ae4-124">Resource Group Name.</span></span>

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

### <span data-ttu-id="85ae4-125">-UserMetadata</span><span class="sxs-lookup"><span data-stu-id="85ae4-125">-UserMetadata</span></span>
<span data-ttu-id="85ae4-126">取得或設定 usermetadata 是一個預留位置，用來儲存 WcfRelay 端點的使用者定義字串資料。例如，它可以用來儲存描述性資料，例如小組清單和連絡人資訊，也可以儲存使用者定義的設定設定。</span><span class="sxs-lookup"><span data-stu-id="85ae4-126">Gets or sets usermetadata is a placeholder to store user-defined string data for the WcfRelay endpoint.e.g. it can be used to store  descriptive data, such as list of teams and their contact information also user-defined configuration settings can be stored.</span></span>

```yaml
Type: System.String
Parameter Sets: WcfRelayPropertiesSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="85ae4-127">-確認</span><span class="sxs-lookup"><span data-stu-id="85ae4-127">-Confirm</span></span>
<span data-ttu-id="85ae4-128">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="85ae4-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="85ae4-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="85ae4-129">-WhatIf</span></span>
<span data-ttu-id="85ae4-130">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="85ae4-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="85ae4-131">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="85ae4-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="85ae4-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85ae4-132">CommonParameters</span></span>
<span data-ttu-id="85ae4-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="85ae4-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85ae4-134">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="85ae4-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85ae4-135">輸入</span><span class="sxs-lookup"><span data-stu-id="85ae4-135">INPUTS</span></span>

### <span data-ttu-id="85ae4-136">System.object</span><span class="sxs-lookup"><span data-stu-id="85ae4-136">System.String</span></span>

### <span data-ttu-id="85ae4-137">PSWcfRelayAttributes 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="85ae4-137">Microsoft.Azure.Commands.Relay.Models.PSWcfRelayAttributes</span></span>

## <span data-ttu-id="85ae4-138">輸出</span><span class="sxs-lookup"><span data-stu-id="85ae4-138">OUTPUTS</span></span>

### <span data-ttu-id="85ae4-139">PSWcfRelayAttributes 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="85ae4-139">Microsoft.Azure.Commands.Relay.Models.PSWcfRelayAttributes</span></span>

## <span data-ttu-id="85ae4-140">筆記</span><span class="sxs-lookup"><span data-stu-id="85ae4-140">NOTES</span></span>

## <span data-ttu-id="85ae4-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="85ae4-141">RELATED LINKS</span></span>
