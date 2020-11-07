---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM.Relay
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/New-AzureRmWcfRelay.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/New-AzureRmWcfRelay.md
ms.openlocfilehash: a7a8734395b08c906b84cc4465528434fcb31eb9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93625079"
---
# <span data-ttu-id="b3353-101">New-AzureRmWcfRelay</span><span class="sxs-lookup"><span data-stu-id="b3353-101">New-AzureRmWcfRelay</span></span>

## <span data-ttu-id="b3353-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b3353-102">SYNOPSIS</span></span>
<span data-ttu-id="b3353-103">在指定的中繼命名空間中建立 WcfRelay。</span><span class="sxs-lookup"><span data-stu-id="b3353-103">Creates a WcfRelay in the specified Relay namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b3353-104">句法</span><span class="sxs-lookup"><span data-stu-id="b3353-104">SYNTAX</span></span>

### <span data-ttu-id="b3353-105">WcfRelayInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="b3353-105">WcfRelayInputObjectSet</span></span>
```
New-AzureRmWcfRelay -ResourceGroupName <String> -Namespace <String> -Name <String>
 [-InputObject <WcfRelayAttributes>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b3353-106">WcfRelayPropertiesSet</span><span class="sxs-lookup"><span data-stu-id="b3353-106">WcfRelayPropertiesSet</span></span>
```
New-AzureRmWcfRelay -ResourceGroupName <String> -Namespace <String> -Name <String> [-WcfRelayType <String>]
 [-RequiresClientAuthorization <Boolean>] [-RequiresTransportSecurity <Boolean>] [-UserMetadata <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b3353-107">說明</span><span class="sxs-lookup"><span data-stu-id="b3353-107">DESCRIPTION</span></span>
<span data-ttu-id="b3353-108">New-AzureRmWcfRelay Cmdlet 會在指定的中繼命名空間中建立 WcfRelay。</span><span class="sxs-lookup"><span data-stu-id="b3353-108">The New-AzureRmWcfRelay cmdlet creates a WcfRelay in the specified Relay namespace.</span></span>

## <span data-ttu-id="b3353-109">示例</span><span class="sxs-lookup"><span data-stu-id="b3353-109">EXAMPLES</span></span>

### <span data-ttu-id="b3353-110">範例 1-InputObject</span><span class="sxs-lookup"><span data-stu-id="b3353-110">Example 1 - InputObject</span></span>
```
PS C:\> $getWcfRelay = Get-AzureRmWcfRelay -ResourceGroupName Default-ServiceBus-WestUS -NamespaceName TestNameSpace-Relay1 -WcfRelayName TestWCFRelay1
PS C:\> $GetWcfRelay.UserMetadata = "TestWCFRelay2"
PS C:\> $GetWcfRelay.RequiresClientAuthorization = $False
PS C:\> $GetWcfRelay.RelayType = "Http"
PS C:\> New-AzureRmWcfRelay -ResourceGroupName Default-Storage-WestUS -Namespace TestNameSpace-Relay1 -Name TestWCFRelay2 -InputObject
```

<span data-ttu-id="b3353-111">\` \` 在指定的中繼命名空間 TestNameSpace 中繼中建立新的 WcfRelay TestWCFRelay2 \` \` 。</span><span class="sxs-lookup"><span data-stu-id="b3353-111">Creates a new WcfRelay \`TestWCFRelay2\` in the specified Relay namespace \`TestNameSpace-Relay\`.</span></span>

### <span data-ttu-id="b3353-112">範例 2-屬性</span><span class="sxs-lookup"><span data-stu-id="b3353-112">Example 2 - Properties</span></span>
```
PS C:\> New-AzureRmWcfRelay -ResourceGroupName Default-Storage-WestUS -Namespace TestNameSpace-Relay1 -Name TestWCFRelay -WcfRelayType "NetTcp"  -RequiresClientAuthorization $True -RequiresTransportSecurity $True -UserMetadata "User Meta data"
```

<span data-ttu-id="b3353-113">\` \` 在指定的中繼命名空間 \` TestNameSpace-Relay1 中建立新的 WcfRelay TestWCFRelay \` 。</span><span class="sxs-lookup"><span data-stu-id="b3353-113">Creates a new WcfRelay \`TestWCFRelay\` in the specified Relay namespace \`TestNameSpace-Relay1\`.</span></span>

## <span data-ttu-id="b3353-114">參數</span><span class="sxs-lookup"><span data-stu-id="b3353-114">PARAMETERS</span></span>

### <span data-ttu-id="b3353-115">-RequiresClientAuthorization</span><span class="sxs-lookup"><span data-stu-id="b3353-115">-RequiresClientAuthorization</span></span>
<span data-ttu-id="b3353-116">如果此中繼需要用戶端授權，則為 true;否則為 false</span><span class="sxs-lookup"><span data-stu-id="b3353-116">true if client authorization is needed for this relay; otherwise, false</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: WcfRelayPropertiesSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3353-117">-RequiresTransportSecurity</span><span class="sxs-lookup"><span data-stu-id="b3353-117">-RequiresTransportSecurity</span></span>
<span data-ttu-id="b3353-118">如果此中繼需要傳輸安全性，則為 true;否則為 false</span><span class="sxs-lookup"><span data-stu-id="b3353-118">true if transport security is needed for this relay; otherwise, false</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: WcfRelayPropertiesSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3353-119">-UserMetadata</span><span class="sxs-lookup"><span data-stu-id="b3353-119">-UserMetadata</span></span>
<span data-ttu-id="b3353-120">取得或設定 usermetadata 是一個預留位置，用來儲存 HybridConnection 端點的使用者定義字串資料。例如，它可以用來儲存描述性資料，例如小組清單和連絡人資訊，也可以儲存使用者定義的設定設定。</span><span class="sxs-lookup"><span data-stu-id="b3353-120">Gets or sets usermetadata is a placeholder to store user-defined string data for the HybridConnection endpoint.e.g. it can be used to store  descriptive data, such as list of teams and their contact information also user-defined configuration settings can be stored.</span></span>

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

### <span data-ttu-id="b3353-121">-WcfRelayType</span><span class="sxs-lookup"><span data-stu-id="b3353-121">-WcfRelayType</span></span>
<span data-ttu-id="b3353-122">WcfRelay 類型。</span><span class="sxs-lookup"><span data-stu-id="b3353-122">WcfRelay Type.</span></span>
<span data-ttu-id="b3353-123">可能的值包括： "NetTcp" 或 "Http"</span><span class="sxs-lookup"><span data-stu-id="b3353-123">Possible values include: 'NetTcp' or 'Http'</span></span>

```yaml
Type: System.String
Parameter Sets: WcfRelayPropertiesSet
Aliases: 
Accepted values: NetTcp, Http

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3353-124">-確認</span><span class="sxs-lookup"><span data-stu-id="b3353-124">-Confirm</span></span>
<span data-ttu-id="b3353-125">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="b3353-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b3353-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b3353-126">-WhatIf</span></span>
<span data-ttu-id="b3353-127">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b3353-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b3353-128">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b3353-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b3353-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b3353-129">-InputObject</span></span>
<span data-ttu-id="b3353-130">WcfRelay 物件。</span><span class="sxs-lookup"><span data-stu-id="b3353-130">WcfRelay object.</span></span>

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

### <span data-ttu-id="b3353-131">-名稱</span><span class="sxs-lookup"><span data-stu-id="b3353-131">-Name</span></span>
<span data-ttu-id="b3353-132">WcfRelay [名稱]。</span><span class="sxs-lookup"><span data-stu-id="b3353-132">WcfRelay Name.</span></span>

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

### <span data-ttu-id="b3353-133">-命名空間</span><span class="sxs-lookup"><span data-stu-id="b3353-133">-Namespace</span></span>
<span data-ttu-id="b3353-134">命名空間名稱。</span><span class="sxs-lookup"><span data-stu-id="b3353-134">Namespace Name.</span></span>

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

### <span data-ttu-id="b3353-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b3353-135">-ResourceGroupName</span></span>
<span data-ttu-id="b3353-136">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="b3353-136">Resource Group Name.</span></span>

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

### <span data-ttu-id="b3353-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3353-137">-DefaultProfile</span></span>
<span data-ttu-id="b3353-138">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="b3353-138">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b3353-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3353-139">CommonParameters</span></span>
<span data-ttu-id="b3353-140">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b3353-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3353-141">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="b3353-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3353-142">輸入</span><span class="sxs-lookup"><span data-stu-id="b3353-142">INPUTS</span></span>

### <span data-ttu-id="b3353-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b3353-143">-ResourceGroupName</span></span>
<span data-ttu-id="b3353-144">System.object</span><span class="sxs-lookup"><span data-stu-id="b3353-144">System.String</span></span>

### <span data-ttu-id="b3353-145">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="b3353-145">-NamespaceName</span></span>
<span data-ttu-id="b3353-146">System.object</span><span class="sxs-lookup"><span data-stu-id="b3353-146">System.String</span></span>

### <span data-ttu-id="b3353-147">-WcfRelayName</span><span class="sxs-lookup"><span data-stu-id="b3353-147">-WcfRelayName</span></span>
<span data-ttu-id="b3353-148">System.object</span><span class="sxs-lookup"><span data-stu-id="b3353-148">System.String</span></span>

### <span data-ttu-id="b3353-149">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b3353-149">-InputObject</span></span>
<span data-ttu-id="b3353-150">WcfRelayAttributes 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="b3353-150">Microsoft.Azure.Commands.Relay.Models.WcfRelayAttributes</span></span>

### <span data-ttu-id="b3353-151">-WcfRelayType</span><span class="sxs-lookup"><span data-stu-id="b3353-151">-WcfRelayType</span></span>
<span data-ttu-id="b3353-152">System.object</span><span class="sxs-lookup"><span data-stu-id="b3353-152">System.String</span></span>

### <span data-ttu-id="b3353-153">-RequiresClientAuthorization</span><span class="sxs-lookup"><span data-stu-id="b3353-153">-RequiresClientAuthorization</span></span>
<span data-ttu-id="b3353-154">System.object</span><span class="sxs-lookup"><span data-stu-id="b3353-154">System.Boolean</span></span>

### <span data-ttu-id="b3353-155">-RequiresTransportSecurity</span><span class="sxs-lookup"><span data-stu-id="b3353-155">-RequiresTransportSecurity</span></span>
<span data-ttu-id="b3353-156">System.object</span><span class="sxs-lookup"><span data-stu-id="b3353-156">System.Boolean</span></span>

### <span data-ttu-id="b3353-157">-UserMetadata</span><span class="sxs-lookup"><span data-stu-id="b3353-157">-UserMetadata</span></span>
<span data-ttu-id="b3353-158">System.object</span><span class="sxs-lookup"><span data-stu-id="b3353-158">System.String</span></span>

## <span data-ttu-id="b3353-159">輸出</span><span class="sxs-lookup"><span data-stu-id="b3353-159">OUTPUTS</span></span>

### <span data-ttu-id="b3353-160">範例 1-InputObject</span><span class="sxs-lookup"><span data-stu-id="b3353-160">Example 1 - InputObject</span></span>

### <span data-ttu-id="b3353-161">WcfRelayAttributes 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="b3353-161">Microsoft.Azure.Commands.Relay.Models.WcfRelayAttributes</span></span>
<span data-ttu-id="b3353-162">RelayType： Http CreatedAt： 4/26/2017 5:14:46 PM UpdatedAt： 4/26/2017 5:14:46 PM ListenerCount： RequiresClientAuthorization： False RequiresTransportSecurity： True IsDynamic： False UserMetadata： TestWCFRelay2 Id：/subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/Default-Storage-WestUS/providers/Microsoft.Rel ay/命名空間/TestNameSpace-Relay1/WcfRelays/TestWCFRelay2 Name： TestWCFRelay2 類型： Microsoft. 中繼/WcfRelays</span><span class="sxs-lookup"><span data-stu-id="b3353-162">RelayType                   : Http CreatedAt                   : 4/26/2017 5:14:46 PM UpdatedAt                   : 4/26/2017 5:14:46 PM ListenerCount               : RequiresClientAuthorization : False RequiresTransportSecurity   : True IsDynamic                   : False UserMetadata                : TestWCFRelay2 Id                          : /subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/Default-Storage-WestUS/providers/Microsoft.Rel ay/namespaces/TestNameSpace-Relay1/WcfRelays/TestWCFRelay2 Name                        : TestWCFRelay2 Type                        : Microsoft.Relay/WcfRelays</span></span>

### <span data-ttu-id="b3353-163">範例 2-屬性</span><span class="sxs-lookup"><span data-stu-id="b3353-163">Example 2 - Properties</span></span>

### <span data-ttu-id="b3353-164">WcfRelayAttributes 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="b3353-164">Microsoft.Azure.Commands.Relay.Models.WcfRelayAttributes</span></span>
<span data-ttu-id="b3353-165">RelayType： NetTcp CreatedAt： 4/26/2017 5:20:08 PM UpdatedAt： 4/26/2017 5:20:08 PM ListenerCount： RequiresClientAuthorization： True RequiresTransportSecurity： True IsDynamic： False UserMetadata： User 中繼資料 Id：/subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/Default-Storage-WestUS/providers/Microsoft.Rel ay/命名空間/TestNameSpace-Relay1/WcfRelays/TestWCFRelay Name： TestWCFRelay 類型： Microsoft. 中繼/WcfRelays</span><span class="sxs-lookup"><span data-stu-id="b3353-165">RelayType                   : NetTcp CreatedAt                   : 4/26/2017 5:20:08 PM UpdatedAt                   : 4/26/2017 5:20:08 PM ListenerCount               : RequiresClientAuthorization : True RequiresTransportSecurity   : True IsDynamic                   : False UserMetadata                : User Meta data Id                          : /subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/Default-Storage-WestUS/providers/Microsoft.Rel ay/namespaces/TestNameSpace-Relay1/WcfRelays/TestWCFRelay Name                        : TestWCFRelay Type                        : Microsoft.Relay/WcfRelays</span></span>

## <span data-ttu-id="b3353-166">筆記</span><span class="sxs-lookup"><span data-stu-id="b3353-166">NOTES</span></span>

## <span data-ttu-id="b3353-167">相關連結</span><span class="sxs-lookup"><span data-stu-id="b3353-167">RELATED LINKS</span></span>
