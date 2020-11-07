---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM.Relay
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Set-AzureRmRelayHybridConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Set-AzureRmRelayHybridConnection.md
ms.openlocfilehash: 7c766d3a112b880eaaa697e1f09d0d458dee5505
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93624782"
---
# <span data-ttu-id="ed480-101">Set-AzureRmRelayHybridConnection</span><span class="sxs-lookup"><span data-stu-id="ed480-101">Set-AzureRmRelayHybridConnection</span></span>

## <span data-ttu-id="ed480-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ed480-102">SYNOPSIS</span></span>
<span data-ttu-id="ed480-103">更新指定的中繼命名空間中 HybridConnection 的描述。</span><span class="sxs-lookup"><span data-stu-id="ed480-103">Updates the description of a HybridConnection in the specified Relay namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ed480-104">句法</span><span class="sxs-lookup"><span data-stu-id="ed480-104">SYNTAX</span></span>

### <span data-ttu-id="ed480-105">HybridConnectionInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="ed480-105">HybridConnectionInputObjectSet</span></span>
```
Set-AzureRmRelayHybridConnection -ResourceGroupName <String> -Namespace <String> -Name <String>
 [-InputObject <HybridConnectionAttibutes>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ed480-106">HybridConnectionPropertiesSet</span><span class="sxs-lookup"><span data-stu-id="ed480-106">HybridConnectionPropertiesSet</span></span>
```
Set-AzureRmRelayHybridConnection -ResourceGroupName <String> -Namespace <String> -Name <String>
 [-UserMetadata <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ed480-107">說明</span><span class="sxs-lookup"><span data-stu-id="ed480-107">DESCRIPTION</span></span>
<span data-ttu-id="ed480-108">Set-AzureRmRelayHybridConnection Cmdlet 會更新指定的中繼命名空間中 HybridConnection 的描述。</span><span class="sxs-lookup"><span data-stu-id="ed480-108">The Set-AzureRmRelayHybridConnection cmdlet updates the description for the HybridConnection in the specified Relay namespace.</span></span>

## <span data-ttu-id="ed480-109">示例</span><span class="sxs-lookup"><span data-stu-id="ed480-109">EXAMPLES</span></span>

### <span data-ttu-id="ed480-110">範例1</span><span class="sxs-lookup"><span data-stu-id="ed480-110">Example 1</span></span>
```
PS C:\>
PS C:\> $GetHybrid = Get-AzureRmRelayHybridConnection -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name TestHybridConnection
PS C:\> $GetHybrid.UserMetadata = "Test UserMetadata"
PS C:\> Set-AzureRmRelayHybridConnection -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name TestHybridConnection -InputObject $GetHybrid
```

### <span data-ttu-id="ed480-111">範例2</span><span class="sxs-lookup"><span data-stu-id="ed480-111">Example 2</span></span>
```
PS C:\> Set-AzureRmRelayHybridConnection -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name TestHybridConnection -UserMetadata = "Test UserMetadata updated"
```

<span data-ttu-id="ed480-112">使用指定命名空間中的新描述更新指定的 HybridConnection。</span><span class="sxs-lookup"><span data-stu-id="ed480-112">Updates the specified HybridConnection with a new description in the specified namespace.</span></span>
<span data-ttu-id="ed480-113">這個範例會使用新的值更新 UserMetadata 屬性。</span><span class="sxs-lookup"><span data-stu-id="ed480-113">This example updates the UserMetadata property with new value.</span></span>

## <span data-ttu-id="ed480-114">參數</span><span class="sxs-lookup"><span data-stu-id="ed480-114">PARAMETERS</span></span>

### <span data-ttu-id="ed480-115">-UserMetadata</span><span class="sxs-lookup"><span data-stu-id="ed480-115">-UserMetadata</span></span>
<span data-ttu-id="ed480-116">取得或設定 usermetadata 是一個預留位置，用來儲存 HybridConnection 端點的使用者定義字串資料。例如，它可以用來儲存描述性資料，例如小組清單和連絡人資訊，也可以儲存使用者定義的設定設定。</span><span class="sxs-lookup"><span data-stu-id="ed480-116">Gets or sets usermetadata is a placeholder to store user-defined string data for the HybridConnection endpoint.e.g. it can be used to store  descriptive data, such as list of teams and their contact information also user-defined configuration settings can be stored.</span></span>

```yaml
Type: System.String
Parameter Sets: HybridConnectionPropertiesSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed480-117">-確認</span><span class="sxs-lookup"><span data-stu-id="ed480-117">-Confirm</span></span>
<span data-ttu-id="ed480-118">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="ed480-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ed480-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ed480-119">-WhatIf</span></span>
<span data-ttu-id="ed480-120">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ed480-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ed480-121">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ed480-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ed480-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ed480-122">-InputObject</span></span>
<span data-ttu-id="ed480-123">HybridConnections 物件。</span><span class="sxs-lookup"><span data-stu-id="ed480-123">HybridConnections object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Relay.Models.HybridConnectionAttibutes
Parameter Sets: HybridConnectionInputObjectSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ed480-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="ed480-124">-Name</span></span>
<span data-ttu-id="ed480-125">HybridConnections [名稱]。</span><span class="sxs-lookup"><span data-stu-id="ed480-125">HybridConnections Name.</span></span>

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

### <span data-ttu-id="ed480-126">-命名空間</span><span class="sxs-lookup"><span data-stu-id="ed480-126">-Namespace</span></span>
<span data-ttu-id="ed480-127">命名空間名稱。</span><span class="sxs-lookup"><span data-stu-id="ed480-127">Namespace Name.</span></span>

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

### <span data-ttu-id="ed480-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ed480-128">-ResourceGroupName</span></span>
<span data-ttu-id="ed480-129">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="ed480-129">Resource Group Name.</span></span>

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

### <span data-ttu-id="ed480-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed480-130">-DefaultProfile</span></span>
<span data-ttu-id="ed480-131">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="ed480-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ed480-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed480-132">CommonParameters</span></span>
<span data-ttu-id="ed480-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ed480-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed480-134">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="ed480-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed480-135">輸入</span><span class="sxs-lookup"><span data-stu-id="ed480-135">INPUTS</span></span>

### <span data-ttu-id="ed480-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ed480-136">-ResourceGroupName</span></span>
<span data-ttu-id="ed480-137">System.object</span><span class="sxs-lookup"><span data-stu-id="ed480-137">System.String</span></span>

### <span data-ttu-id="ed480-138">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="ed480-138">-NamespaceName</span></span>
<span data-ttu-id="ed480-139">System.object</span><span class="sxs-lookup"><span data-stu-id="ed480-139">System.String</span></span>

### <span data-ttu-id="ed480-140">-WcfRelayName</span><span class="sxs-lookup"><span data-stu-id="ed480-140">-WcfRelayName</span></span>
<span data-ttu-id="ed480-141">System.object</span><span class="sxs-lookup"><span data-stu-id="ed480-141">System.String</span></span>

### <span data-ttu-id="ed480-142">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ed480-142">-InputObject</span></span>
<span data-ttu-id="ed480-143">HybridConnectionAttibutes 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="ed480-143">Microsoft.Azure.Commands.Relay.Models.HybridConnectionAttibutes</span></span>

### <span data-ttu-id="ed480-144">-UserMetadata</span><span class="sxs-lookup"><span data-stu-id="ed480-144">-UserMetadata</span></span>
<span data-ttu-id="ed480-145">System.object</span><span class="sxs-lookup"><span data-stu-id="ed480-145">System.String</span></span>

## <span data-ttu-id="ed480-146">輸出</span><span class="sxs-lookup"><span data-stu-id="ed480-146">OUTPUTS</span></span>

### <span data-ttu-id="ed480-147">範例-1： InputObject</span><span class="sxs-lookup"><span data-stu-id="ed480-147">Examples - 1 : InputObject</span></span>
<span data-ttu-id="ed480-148">CreatedAt： 4/26/2017 10:04:15 PM UpdatedAt： 4/26/2017 10:08:11 PM ListenerCount： RequiresClientAuthorization： True UserMetadata： Test UserMetadata Id：/subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-HybirdConnection/HybridConnections/TestHybirdConnectio n2 Name： TestHybirdConnection2 類型： Microsoft. 中繼/HybridConnections</span><span class="sxs-lookup"><span data-stu-id="ed480-148">CreatedAt                   : 4/26/2017 10:04:15 PM UpdatedAt                   : 4/26/2017 10:08:11 PM ListenerCount               : RequiresClientAuthorization : True UserMetadata                : Test UserMetadata Id                          : /subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/Default-ServiceBus-WestUS /providers/Microsoft.Relay/namespaces/TestNameSpace-HybirdConnection/HybridConnections/TestHybirdConnectio n2 Name                        : TestHybirdConnection2 Type                        : Microsoft.Relay/HybridConnections</span></span>

### <span data-ttu-id="ed480-149">範例-2：屬性</span><span class="sxs-lookup"><span data-stu-id="ed480-149">Examples - 2 : Properties</span></span>
<span data-ttu-id="ed480-150">CreatedAt： 4/26/2017 10:04:15 PM UpdatedAt： 4/26/2017 10:10:25 PM ListenerCount： RequiresClientAuthorization： True UserMetadata： Test UserMetadata 已更新的 Id：/subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-HybirdConnection/HybridConnections/TestHybirdConnectio n1 Name： TestHybirdConnection1 類型： Microsoft. 中繼/HybridConnections</span><span class="sxs-lookup"><span data-stu-id="ed480-150">CreatedAt                   : 4/26/2017 10:04:15 PM UpdatedAt                   : 4/26/2017 10:10:25 PM ListenerCount               : RequiresClientAuthorization : True UserMetadata                : Test UserMetadata updated Id                          : /subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/Default-ServiceBus-WestUS /providers/Microsoft.Relay/namespaces/TestNameSpace-HybirdConnection/HybridConnections/TestHybirdConnectio n1 Name                        : TestHybirdConnection1 Type                        : Microsoft.Relay/HybridConnections</span></span>

## <span data-ttu-id="ed480-151">筆記</span><span class="sxs-lookup"><span data-stu-id="ed480-151">NOTES</span></span>

## <span data-ttu-id="ed480-152">相關連結</span><span class="sxs-lookup"><span data-stu-id="ed480-152">RELATED LINKS</span></span>

