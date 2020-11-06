---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.relay/set-azurermwcfrelay
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Set-AzureRmWcfRelay.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Set-AzureRmWcfRelay.md
ms.openlocfilehash: 16df81633d4265b7b52dd2678bb58c80d4a756e0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93447685"
---
# <span data-ttu-id="fea58-101">Set-AzureRmWcfRelay</span><span class="sxs-lookup"><span data-stu-id="fea58-101">Set-AzureRmWcfRelay</span></span>

## <span data-ttu-id="fea58-102">摘要</span><span class="sxs-lookup"><span data-stu-id="fea58-102">SYNOPSIS</span></span>
<span data-ttu-id="fea58-103">更新指定的中繼命名空間中 WcfRelay 的描述。</span><span class="sxs-lookup"><span data-stu-id="fea58-103">Updates the description of a WcfRelay in the specified Relay namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fea58-104">句法</span><span class="sxs-lookup"><span data-stu-id="fea58-104">SYNTAX</span></span>

### <span data-ttu-id="fea58-105">WcfRelayInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="fea58-105">WcfRelayInputObjectSet</span></span>
```
Set-AzureRmWcfRelay [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-InputObject <WcfRelayAttributes>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fea58-106">WcfRelayPropertiesSet</span><span class="sxs-lookup"><span data-stu-id="fea58-106">WcfRelayPropertiesSet</span></span>
```
Set-AzureRmWcfRelay [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-UserMetadata <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fea58-107">說明</span><span class="sxs-lookup"><span data-stu-id="fea58-107">DESCRIPTION</span></span>
<span data-ttu-id="fea58-108">Set-AzureRmWcfRelay Cmdlet 會更新指定的中繼命名空間中 WcfRelay 的描述。</span><span class="sxs-lookup"><span data-stu-id="fea58-108">The Set-AzureRmWcfRelay cmdlet updates the description for the WcfRelay in the specified Relay namespace.</span></span>

## <span data-ttu-id="fea58-109">示例</span><span class="sxs-lookup"><span data-stu-id="fea58-109">EXAMPLES</span></span>

### <span data-ttu-id="fea58-110">範例 1-InputObject</span><span class="sxs-lookup"><span data-stu-id="fea58-110">Example 1 - InputObject</span></span>
```
PS C:\>
PS C:\> $getWcfRelay = Get-AzureRmWcfRelay -ResourceGroupName Default-ServiceBus-WestUS -NamespaceName TestNameSpace-Relay1 -WcfRelayName TestWCFRelay
PS C:\> $getWcfRelay.UserMetadata = "usermetadata is a placeholder to store user-defined string data for the HybridConnection endpoint.e.g. it can be used to store  desc
riptive data, such as list of teams and their contact information also user-defined configuration settings can be stored."
PS C:\> Set-AzureRmWcfRelay -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name TestWCFRelay1 -InputObject $getWcfRelay
```

### <span data-ttu-id="fea58-111">範例 2-屬性</span><span class="sxs-lookup"><span data-stu-id="fea58-111">Example 2 - Properties</span></span>
```
PS C:\> Set-AzureRmWcfRelay -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name TestWCFRelay1 -UserMetadata "User Meta data"
```

<span data-ttu-id="fea58-112">使用指定命名空間中的新描述更新指定的 WcfRelay。</span><span class="sxs-lookup"><span data-stu-id="fea58-112">Updates the specified WcfRelay with a new description in the specified namespace.</span></span>
<span data-ttu-id="fea58-113">這個範例會使用新的值更新 UserMetadata 屬性。</span><span class="sxs-lookup"><span data-stu-id="fea58-113">This example updates the UserMetadata property with new value.</span></span>

## <span data-ttu-id="fea58-114">參數</span><span class="sxs-lookup"><span data-stu-id="fea58-114">PARAMETERS</span></span>

### <span data-ttu-id="fea58-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fea58-115">-DefaultProfile</span></span>
<span data-ttu-id="fea58-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="fea58-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fea58-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fea58-117">-InputObject</span></span>
<span data-ttu-id="fea58-118">WcfRelay 物件。</span><span class="sxs-lookup"><span data-stu-id="fea58-118">WcfRelay object.</span></span>

```yaml
Type: WcfRelayAttributes
Parameter Sets: WcfRelayInputObjectSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fea58-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="fea58-119">-Name</span></span>
<span data-ttu-id="fea58-120">WcfRelay [名稱]。</span><span class="sxs-lookup"><span data-stu-id="fea58-120">WcfRelay Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fea58-121">-命名空間</span><span class="sxs-lookup"><span data-stu-id="fea58-121">-Namespace</span></span>
<span data-ttu-id="fea58-122">命名空間名稱。</span><span class="sxs-lookup"><span data-stu-id="fea58-122">Namespace Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fea58-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fea58-123">-ResourceGroupName</span></span>
<span data-ttu-id="fea58-124">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="fea58-124">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fea58-125">-UserMetadata</span><span class="sxs-lookup"><span data-stu-id="fea58-125">-UserMetadata</span></span>
<span data-ttu-id="fea58-126">取得或設定 usermetadata 是一個預留位置，用來儲存 HybridConnection 端點的使用者定義字串資料。例如，它可以用來儲存描述性資料，例如小組清單和連絡人資訊，也可以儲存使用者定義的設定設定。</span><span class="sxs-lookup"><span data-stu-id="fea58-126">Gets or sets usermetadata is a placeholder to store user-defined string data for the HybridConnection endpoint.e.g. it can be used to store  descriptive data, such as list of teams and their contact information also user-defined configuration settings can be stored.</span></span>

```yaml
Type: String
Parameter Sets: WcfRelayPropertiesSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fea58-127">-確認</span><span class="sxs-lookup"><span data-stu-id="fea58-127">-Confirm</span></span>
<span data-ttu-id="fea58-128">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="fea58-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fea58-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fea58-129">-WhatIf</span></span>
<span data-ttu-id="fea58-130">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="fea58-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fea58-131">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="fea58-131">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fea58-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fea58-132">CommonParameters</span></span>
<span data-ttu-id="fea58-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="fea58-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fea58-134">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="fea58-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fea58-135">輸入</span><span class="sxs-lookup"><span data-stu-id="fea58-135">INPUTS</span></span>

### <span data-ttu-id="fea58-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fea58-136">-ResourceGroupName</span></span>
<span data-ttu-id="fea58-137">System.object</span><span class="sxs-lookup"><span data-stu-id="fea58-137">System.String</span></span>

### <span data-ttu-id="fea58-138">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="fea58-138">-NamespaceName</span></span>
<span data-ttu-id="fea58-139">System.object</span><span class="sxs-lookup"><span data-stu-id="fea58-139">System.String</span></span>

### <span data-ttu-id="fea58-140">-WcfRelayName</span><span class="sxs-lookup"><span data-stu-id="fea58-140">-WcfRelayName</span></span>
<span data-ttu-id="fea58-141">System.object</span><span class="sxs-lookup"><span data-stu-id="fea58-141">System.String</span></span>

### <span data-ttu-id="fea58-142">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fea58-142">-InputObject</span></span>
<span data-ttu-id="fea58-143">WcfRelayAttributes 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="fea58-143">Microsoft.Azure.Commands.Relay.Models.WcfRelayAttributes</span></span>

### <span data-ttu-id="fea58-144">-WcfRelayType</span><span class="sxs-lookup"><span data-stu-id="fea58-144">-WcfRelayType</span></span>
<span data-ttu-id="fea58-145">System.object</span><span class="sxs-lookup"><span data-stu-id="fea58-145">System.String</span></span>

### <span data-ttu-id="fea58-146">-UserMetadata</span><span class="sxs-lookup"><span data-stu-id="fea58-146">-UserMetadata</span></span>
<span data-ttu-id="fea58-147">System.object</span><span class="sxs-lookup"><span data-stu-id="fea58-147">System.String</span></span>

## <span data-ttu-id="fea58-148">輸出</span><span class="sxs-lookup"><span data-stu-id="fea58-148">OUTPUTS</span></span>

### <span data-ttu-id="fea58-149">WcfRelayAttributes 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="fea58-149">Microsoft.Azure.Commands.Relay.Models.WcfRelayAttributes</span></span>

### <span data-ttu-id="fea58-150">範例 1-InputObject</span><span class="sxs-lookup"><span data-stu-id="fea58-150">Example 1 - InputObject</span></span>

### <span data-ttu-id="fea58-151">WcfRelayAttributes 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="fea58-151">Microsoft.Azure.Commands.Relay.Models.WcfRelayAttributes</span></span>
<span data-ttu-id="fea58-152">RelayType： Http CreatedAt： 4/26/2017 5:14:46 PM UpdatedAt： 4/26/2017 5:16:50 PM ListenerCount： RequiresClientAuthorization： False RequiresTransportSecurity： True IsDynamic： False UserMetadata： UserMetadata 是儲存在 HybridConnection 端點的使用者定義字串資料的預留位置。例如，它可以用來儲存 desc riptive 資料，例如小組清單和連絡人資訊，也可以儲存使用者定義的設定設定。</span><span class="sxs-lookup"><span data-stu-id="fea58-152">RelayType                   : Http CreatedAt                   : 4/26/2017 5:14:46 PM UpdatedAt                   : 4/26/2017 5:16:50 PM ListenerCount               : RequiresClientAuthorization : False RequiresTransportSecurity   : True IsDynamic                   : False UserMetadata                : usermetadata is a placeholder to store user-defined string data for the HybridConnection endpoint.e.g. it can be used to store  desc riptive data, such as list of teams and their contact information also user-defined configuration settings can be stored.</span></span>
<span data-ttu-id="fea58-153">識別碼：/subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/Default-Storage-WestUS/providers/Microsoft.Rel ay/命名空間/TestNameSpace-Relay1/WcfRelays/TestWCFRelay2 Name： TestWCFRelay2 類型： Microsoft. 中繼/WcfRelays</span><span class="sxs-lookup"><span data-stu-id="fea58-153">Id                          : /subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/Default-Storage-WestUS/providers/Microsoft.Rel ay/namespaces/TestNameSpace-Relay1/WcfRelays/TestWCFRelay2 Name                        : TestWCFRelay2 Type                        : Microsoft.Relay/WcfRelays</span></span>

### <span data-ttu-id="fea58-154">範例 2-屬性</span><span class="sxs-lookup"><span data-stu-id="fea58-154">Example 2 - Properties</span></span>

### <span data-ttu-id="fea58-155">WcfRelayAttributes 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="fea58-155">Microsoft.Azure.Commands.Relay.Models.WcfRelayAttributes</span></span>
<span data-ttu-id="fea58-156">RelayType： NetTcp CreatedAt： 4/26/2017 5:20:08 PM UpdatedAt： 4/26/2017 5:26:09 PM ListenerCount： RequiresClientAuthorization： True RequiresTransportSecurity： True IsDynamic： False UserMetadata： User 中繼資料 Id：/subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/Default-Storage-WestUS/providers/Microsoft.Rel ay/命名空間/TestNameSpace-Relay1/WcfRelays/TestWCFRelay Name： TestWCFRelay 類型： Microsoft. 中繼/WcfRelays</span><span class="sxs-lookup"><span data-stu-id="fea58-156">RelayType                   : NetTcp CreatedAt                   : 4/26/2017 5:20:08 PM UpdatedAt                   : 4/26/2017 5:26:09 PM ListenerCount               : RequiresClientAuthorization : True RequiresTransportSecurity   : True IsDynamic                   : False UserMetadata                : User Meta data Id                          : /subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/Default-Storage-WestUS/providers/Microsoft.Rel ay/namespaces/TestNameSpace-Relay1/WcfRelays/TestWCFRelay Name                        : TestWCFRelay Type                        : Microsoft.Relay/WcfRelays</span></span>

## <span data-ttu-id="fea58-157">筆記</span><span class="sxs-lookup"><span data-stu-id="fea58-157">NOTES</span></span>

## <span data-ttu-id="fea58-158">相關連結</span><span class="sxs-lookup"><span data-stu-id="fea58-158">RELATED LINKS</span></span>

