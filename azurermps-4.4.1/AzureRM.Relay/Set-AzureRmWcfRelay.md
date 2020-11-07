---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM.Relay
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Set-AzureRmWcfRelay.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Set-AzureRmWcfRelay.md
ms.openlocfilehash: af4927631b126f068495b3b130dfc560874834cb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93623645"
---
# <span data-ttu-id="4c9d3-101">Set-AzureRmWcfRelay</span><span class="sxs-lookup"><span data-stu-id="4c9d3-101">Set-AzureRmWcfRelay</span></span>

## <span data-ttu-id="4c9d3-102">摘要</span><span class="sxs-lookup"><span data-stu-id="4c9d3-102">SYNOPSIS</span></span>
<span data-ttu-id="4c9d3-103">更新指定的中繼命名空間中 WcfRelay 的描述。</span><span class="sxs-lookup"><span data-stu-id="4c9d3-103">Updates the description of a WcfRelay in the specified Relay namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4c9d3-104">句法</span><span class="sxs-lookup"><span data-stu-id="4c9d3-104">SYNTAX</span></span>

### <span data-ttu-id="4c9d3-105">WcfRelayInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="4c9d3-105">WcfRelayInputObjectSet</span></span>
```
Set-AzureRmWcfRelay -ResourceGroupName <String> -Namespace <String> -Name <String>
 [-InputObject <WcfRelayAttributes>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4c9d3-106">WcfRelayPropertiesSet</span><span class="sxs-lookup"><span data-stu-id="4c9d3-106">WcfRelayPropertiesSet</span></span>
```
Set-AzureRmWcfRelay -ResourceGroupName <String> -Namespace <String> -Name <String> [-UserMetadata <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4c9d3-107">說明</span><span class="sxs-lookup"><span data-stu-id="4c9d3-107">DESCRIPTION</span></span>
<span data-ttu-id="4c9d3-108">Set-AzureRmWcfRelay Cmdlet 會更新指定的中繼命名空間中 WcfRelay 的描述。</span><span class="sxs-lookup"><span data-stu-id="4c9d3-108">The Set-AzureRmWcfRelay cmdlet updates the description for the WcfRelay in the specified Relay namespace.</span></span>

## <span data-ttu-id="4c9d3-109">示例</span><span class="sxs-lookup"><span data-stu-id="4c9d3-109">EXAMPLES</span></span>

### <span data-ttu-id="4c9d3-110">範例 1-InputObject</span><span class="sxs-lookup"><span data-stu-id="4c9d3-110">Example 1 - InputObject</span></span>
```
PS C:\>
PS C:\> $getWcfRelay = Get-AzureRmWcfRelay -ResourceGroupName Default-ServiceBus-WestUS -NamespaceName TestNameSpace-Relay1 -WcfRelayName TestWCFRelay
PS C:\> $getWcfRelay.UserMetadata = "usermetadata is a placeholder to store user-defined string data for the HybridConnection endpoint.e.g. it can be used to store  desc
riptive data, such as list of teams and their contact information also user-defined configuration settings can be stored."
PS C:\> Set-AzureRmWcfRelay -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name TestWCFRelay1 -InputObject $getWcfRelay
```

### <span data-ttu-id="4c9d3-111">範例 2-屬性</span><span class="sxs-lookup"><span data-stu-id="4c9d3-111">Example 2 - Properties</span></span>
```
PS C:\> Set-AzureRmWcfRelay -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name TestWCFRelay1 -UserMetadata "User Meta data"
```

<span data-ttu-id="4c9d3-112">使用指定命名空間中的新描述更新指定的 WcfRelay。</span><span class="sxs-lookup"><span data-stu-id="4c9d3-112">Updates the specified WcfRelay with a new description in the specified namespace.</span></span>
<span data-ttu-id="4c9d3-113">這個範例會使用新的值更新 UserMetadata 屬性。</span><span class="sxs-lookup"><span data-stu-id="4c9d3-113">This example updates the UserMetadata property with new value.</span></span>

## <span data-ttu-id="4c9d3-114">參數</span><span class="sxs-lookup"><span data-stu-id="4c9d3-114">PARAMETERS</span></span>

### <span data-ttu-id="4c9d3-115">-UserMetadata</span><span class="sxs-lookup"><span data-stu-id="4c9d3-115">-UserMetadata</span></span>
<span data-ttu-id="4c9d3-116">取得或設定 usermetadata 是一個預留位置，用來儲存 HybridConnection 端點的使用者定義字串資料。例如，它可以用來儲存描述性資料，例如小組清單和連絡人資訊，也可以儲存使用者定義的設定設定。</span><span class="sxs-lookup"><span data-stu-id="4c9d3-116">Gets or sets usermetadata is a placeholder to store user-defined string data for the HybridConnection endpoint.e.g. it can be used to store  descriptive data, such as list of teams and their contact information also user-defined configuration settings can be stored.</span></span>

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

### <span data-ttu-id="4c9d3-117">-確認</span><span class="sxs-lookup"><span data-stu-id="4c9d3-117">-Confirm</span></span>
<span data-ttu-id="4c9d3-118">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="4c9d3-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c9d3-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4c9d3-119">-WhatIf</span></span>
<span data-ttu-id="4c9d3-120">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="4c9d3-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4c9d3-121">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="4c9d3-121">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c9d3-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4c9d3-122">-InputObject</span></span>
<span data-ttu-id="4c9d3-123">WcfRelay 物件。</span><span class="sxs-lookup"><span data-stu-id="4c9d3-123">WcfRelay object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Relay.Models.WcfRelayAttributes
Parameter Sets: WcfRelayInputObjectSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4c9d3-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="4c9d3-124">-Name</span></span>
<span data-ttu-id="4c9d3-125">WcfRelay [名稱]。</span><span class="sxs-lookup"><span data-stu-id="4c9d3-125">WcfRelay Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4c9d3-126">-命名空間</span><span class="sxs-lookup"><span data-stu-id="4c9d3-126">-Namespace</span></span>
<span data-ttu-id="4c9d3-127">命名空間名稱。</span><span class="sxs-lookup"><span data-stu-id="4c9d3-127">Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4c9d3-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4c9d3-128">-ResourceGroupName</span></span>
<span data-ttu-id="4c9d3-129">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="4c9d3-129">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4c9d3-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4c9d3-130">-DefaultProfile</span></span>
<span data-ttu-id="4c9d3-131">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="4c9d3-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4c9d3-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c9d3-132">CommonParameters</span></span>
<span data-ttu-id="4c9d3-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="4c9d3-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c9d3-134">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="4c9d3-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c9d3-135">輸入</span><span class="sxs-lookup"><span data-stu-id="4c9d3-135">INPUTS</span></span>

### <span data-ttu-id="4c9d3-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4c9d3-136">-ResourceGroupName</span></span>
<span data-ttu-id="4c9d3-137">System.object</span><span class="sxs-lookup"><span data-stu-id="4c9d3-137">System.String</span></span>

### <span data-ttu-id="4c9d3-138">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="4c9d3-138">-NamespaceName</span></span>
<span data-ttu-id="4c9d3-139">System.object</span><span class="sxs-lookup"><span data-stu-id="4c9d3-139">System.String</span></span>

### <span data-ttu-id="4c9d3-140">-WcfRelayName</span><span class="sxs-lookup"><span data-stu-id="4c9d3-140">-WcfRelayName</span></span>
<span data-ttu-id="4c9d3-141">System.object</span><span class="sxs-lookup"><span data-stu-id="4c9d3-141">System.String</span></span>

### <span data-ttu-id="4c9d3-142">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4c9d3-142">-InputObject</span></span>
<span data-ttu-id="4c9d3-143">WcfRelayAttributes 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="4c9d3-143">Microsoft.Azure.Commands.Relay.Models.WcfRelayAttributes</span></span>

### <span data-ttu-id="4c9d3-144">-WcfRelayType</span><span class="sxs-lookup"><span data-stu-id="4c9d3-144">-WcfRelayType</span></span>
<span data-ttu-id="4c9d3-145">System.object</span><span class="sxs-lookup"><span data-stu-id="4c9d3-145">System.String</span></span>

### <span data-ttu-id="4c9d3-146">-UserMetadata</span><span class="sxs-lookup"><span data-stu-id="4c9d3-146">-UserMetadata</span></span>
<span data-ttu-id="4c9d3-147">System.object</span><span class="sxs-lookup"><span data-stu-id="4c9d3-147">System.String</span></span>

## <span data-ttu-id="4c9d3-148">輸出</span><span class="sxs-lookup"><span data-stu-id="4c9d3-148">OUTPUTS</span></span>

### <span data-ttu-id="4c9d3-149">WcfRelayAttributes 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="4c9d3-149">Microsoft.Azure.Commands.Relay.Models.WcfRelayAttributes</span></span>

### <span data-ttu-id="4c9d3-150">範例 1-InputObject</span><span class="sxs-lookup"><span data-stu-id="4c9d3-150">Example 1 - InputObject</span></span>

### <span data-ttu-id="4c9d3-151">WcfRelayAttributes 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="4c9d3-151">Microsoft.Azure.Commands.Relay.Models.WcfRelayAttributes</span></span>
<span data-ttu-id="4c9d3-152">RelayType： Http CreatedAt： 4/26/2017 5:14:46 PM UpdatedAt： 4/26/2017 5:16:50 PM ListenerCount： RequiresClientAuthorization： False RequiresTransportSecurity： True IsDynamic： False UserMetadata： UserMetadata 是儲存在 HybridConnection 端點的使用者定義字串資料的預留位置。例如，它可以用來儲存 desc riptive 資料，例如小組清單和連絡人資訊，也可以儲存使用者定義的設定設定。</span><span class="sxs-lookup"><span data-stu-id="4c9d3-152">RelayType                   : Http CreatedAt                   : 4/26/2017 5:14:46 PM UpdatedAt                   : 4/26/2017 5:16:50 PM ListenerCount               : RequiresClientAuthorization : False RequiresTransportSecurity   : True IsDynamic                   : False UserMetadata                : usermetadata is a placeholder to store user-defined string data for the HybridConnection endpoint.e.g. it can be used to store  desc riptive data, such as list of teams and their contact information also user-defined configuration settings can be stored.</span></span>
<span data-ttu-id="4c9d3-153">識別碼：/subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/Default-Storage-WestUS/providers/Microsoft.Rel ay/命名空間/TestNameSpace-Relay1/WcfRelays/TestWCFRelay2 Name： TestWCFRelay2 類型： Microsoft. 中繼/WcfRelays</span><span class="sxs-lookup"><span data-stu-id="4c9d3-153">Id                          : /subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/Default-Storage-WestUS/providers/Microsoft.Rel ay/namespaces/TestNameSpace-Relay1/WcfRelays/TestWCFRelay2 Name                        : TestWCFRelay2 Type                        : Microsoft.Relay/WcfRelays</span></span>

### <span data-ttu-id="4c9d3-154">範例 2-屬性</span><span class="sxs-lookup"><span data-stu-id="4c9d3-154">Example 2 - Properties</span></span>

### <span data-ttu-id="4c9d3-155">WcfRelayAttributes 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="4c9d3-155">Microsoft.Azure.Commands.Relay.Models.WcfRelayAttributes</span></span>
<span data-ttu-id="4c9d3-156">RelayType： NetTcp CreatedAt： 4/26/2017 5:20:08 PM UpdatedAt： 4/26/2017 5:26:09 PM ListenerCount： RequiresClientAuthorization： True RequiresTransportSecurity： True IsDynamic： False UserMetadata： User 中繼資料 Id：/subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/Default-Storage-WestUS/providers/Microsoft.Rel ay/命名空間/TestNameSpace-Relay1/WcfRelays/TestWCFRelay Name： TestWCFRelay 類型： Microsoft. 中繼/WcfRelays</span><span class="sxs-lookup"><span data-stu-id="4c9d3-156">RelayType                   : NetTcp CreatedAt                   : 4/26/2017 5:20:08 PM UpdatedAt                   : 4/26/2017 5:26:09 PM ListenerCount               : RequiresClientAuthorization : True RequiresTransportSecurity   : True IsDynamic                   : False UserMetadata                : User Meta data Id                          : /subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/Default-Storage-WestUS/providers/Microsoft.Rel ay/namespaces/TestNameSpace-Relay1/WcfRelays/TestWCFRelay Name                        : TestWCFRelay Type                        : Microsoft.Relay/WcfRelays</span></span>

## <span data-ttu-id="4c9d3-157">筆記</span><span class="sxs-lookup"><span data-stu-id="4c9d3-157">NOTES</span></span>

## <span data-ttu-id="4c9d3-158">相關連結</span><span class="sxs-lookup"><span data-stu-id="4c9d3-158">RELATED LINKS</span></span>

