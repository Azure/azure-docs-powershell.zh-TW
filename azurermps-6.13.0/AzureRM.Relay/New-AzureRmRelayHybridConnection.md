---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.relay/new-azurermrelayhybridconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/New-AzureRmRelayHybridConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/New-AzureRmRelayHybridConnection.md
ms.openlocfilehash: 1caf26a439cdc835d511ffb7bd6021dd5db1fa9b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93445511"
---
# <span data-ttu-id="29385-101">New-AzureRmRelayHybridConnection</span><span class="sxs-lookup"><span data-stu-id="29385-101">New-AzureRmRelayHybridConnection</span></span>

## <span data-ttu-id="29385-102">摘要</span><span class="sxs-lookup"><span data-stu-id="29385-102">SYNOPSIS</span></span>
<span data-ttu-id="29385-103">在指定的中繼命名空間中建立 HybridConnection。</span><span class="sxs-lookup"><span data-stu-id="29385-103">Creates a HybridConnection in the specified Relay namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="29385-104">句法</span><span class="sxs-lookup"><span data-stu-id="29385-104">SYNTAX</span></span>

### <span data-ttu-id="29385-105">HybridConnectionInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="29385-105">HybridConnectionInputObjectSet</span></span>
```
New-AzureRmRelayHybridConnection [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-InputObject <HybridConnectionAttibutes>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="29385-106">HybridConnectionPropertiesSet</span><span class="sxs-lookup"><span data-stu-id="29385-106">HybridConnectionPropertiesSet</span></span>
```
New-AzureRmRelayHybridConnection [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-RequiresClientAuthorization <Boolean>] [-UserMetadata <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="29385-107">說明</span><span class="sxs-lookup"><span data-stu-id="29385-107">DESCRIPTION</span></span>
<span data-ttu-id="29385-108">New-AzureRmRelayHybridConnection Cmdlet 會在指定的中繼命名空間中建立 HybridConnection。</span><span class="sxs-lookup"><span data-stu-id="29385-108">The New-AzureRmRelayHybridConnection cmdlet creates a HybridConnection in the specified Relay namespace.</span></span>

## <span data-ttu-id="29385-109">示例</span><span class="sxs-lookup"><span data-stu-id="29385-109">EXAMPLES</span></span>

### <span data-ttu-id="29385-110">範例 1-InputObject</span><span class="sxs-lookup"><span data-stu-id="29385-110">Example 1 - InputObject</span></span>
```
PS C:\> $getHybirdConnection = Get-AzureRmRelayHybridConnection -ResourceGroupName Default-ServiceBus-WestUS -NamespaceName TestNameSpace-HybirdConnection -Name TestHybirdConnection1
PS C:\> $getHybirdConnection.UserMetadata = "TestHybirdConnection2"
PS C:\> $getHybirdConnection.RequiresClientAuthorization = $False
PS C:\> New-AzureRmRelayHybridConnection -ResourceGroupName Default-Storage-WestUS -Namespace TestNameSpace-HybirdConnection -Name TestHybirdConnection2 -InputObject $getHybirdConnection

CreatedAt                   : 4/26/2017 10:04:15 PM
UpdatedAt                   : 4/26/2017 10:04:15 PM
ListenerCount               :
RequiresClientAuthorization : True
UserMetadata                : User Meta data
Id                          : /subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/Default-ServiceBus-WestUS
                              /providers/Microsoft.Relay/namespaces/TestNameSpace-HybirdConnection/HybridConnections/TestHybirdConnectio
                              n2
Name                        : TestHybirdConnection2
Type                        : Microsoft.Relay/HybridConnections
```

<span data-ttu-id="29385-111">\` \` 在指定的中繼命名空間 \` TestNameSpace-HybirdConnection 中建立新的 HybirdConnection TestHybirdConnection2 \` 。</span><span class="sxs-lookup"><span data-stu-id="29385-111">Creates a new HybirdConnection \`TestHybirdConnection2\` in the specified Relay namespace \`TestNameSpace-HybirdConnection\`.</span></span>

### <span data-ttu-id="29385-112">範例 2-屬性</span><span class="sxs-lookup"><span data-stu-id="29385-112">Example 2 - Properties</span></span>
```
PS C:\> New-AzureRmWcfRelay -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-HybirdConnection -Name TestHybirdConnection1 -RequiresClientAuthorization $True -UserMetadata "User Meta data"

CreatedAt                   : 4/26/2017 10:04:15 PM
UpdatedAt                   : 4/26/2017 10:04:15 PM
ListenerCount               :
RequiresClientAuthorization : True
UserMetadata                : User Meta data
Id                          : /subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/Default-ServiceBus-WestUS
                              /providers/Microsoft.Relay/namespaces/TestNameSpace-HybirdConnection/HybridConnections/TestHybirdConnectio
                              n1
Name                        : TestHybirdConnection1
Type                        : Microsoft.Relay/HybridConnections
```

<span data-ttu-id="29385-113">\` \` 在指定的中繼命名空間 \` TestNameSpace-HybirdConnection 中建立新的 HybirdConnection TestHybirdConnection1 \` 。</span><span class="sxs-lookup"><span data-stu-id="29385-113">Creates a new HybirdConnection \`TestHybirdConnection1\` in the specified Relay namespace \`TestNameSpace-HybirdConnection\`.</span></span>

## <span data-ttu-id="29385-114">參數</span><span class="sxs-lookup"><span data-stu-id="29385-114">PARAMETERS</span></span>

### <span data-ttu-id="29385-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29385-115">-DefaultProfile</span></span>
<span data-ttu-id="29385-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="29385-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="29385-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="29385-117">-InputObject</span></span>
<span data-ttu-id="29385-118">HybridConnections 物件。</span><span class="sxs-lookup"><span data-stu-id="29385-118">HybridConnections object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Relay.Models.PSHybridConnectionAttibutes
Parameter Sets: HybridConnectionInputObjectSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="29385-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="29385-119">-Name</span></span>
<span data-ttu-id="29385-120">HybridConnections [名稱]。</span><span class="sxs-lookup"><span data-stu-id="29385-120">HybridConnections Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="29385-121">-命名空間</span><span class="sxs-lookup"><span data-stu-id="29385-121">-Namespace</span></span>
<span data-ttu-id="29385-122">命名空間名稱。</span><span class="sxs-lookup"><span data-stu-id="29385-122">Namespace Name.</span></span>

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

### <span data-ttu-id="29385-123">-RequiresClientAuthorization</span><span class="sxs-lookup"><span data-stu-id="29385-123">-RequiresClientAuthorization</span></span>
<span data-ttu-id="29385-124">如果此 HybridConnections 需要用戶端授權，則為 true;否則為 false</span><span class="sxs-lookup"><span data-stu-id="29385-124">true if client authorization is needed for this HybridConnections; otherwise, false</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: HybridConnectionPropertiesSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="29385-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="29385-125">-ResourceGroupName</span></span>
<span data-ttu-id="29385-126">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="29385-126">Resource Group Name.</span></span>

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

### <span data-ttu-id="29385-127">-UserMetadata</span><span class="sxs-lookup"><span data-stu-id="29385-127">-UserMetadata</span></span>
<span data-ttu-id="29385-128">取得或設定 usermetadata 是一個預留位置，用來儲存 HybridConnection 端點的使用者定義字串資料。例如，它可以用來儲存描述性資料，例如小組清單和連絡人資訊，也可以儲存使用者定義的設定設定。</span><span class="sxs-lookup"><span data-stu-id="29385-128">Gets or sets usermetadata is a placeholder to store user-defined string data for the HybridConnection endpoint.e.g. it can be used to store  descriptive data, such as list of teams and their contact information also user-defined configuration settings can be stored.</span></span>

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

### <span data-ttu-id="29385-129">-確認</span><span class="sxs-lookup"><span data-stu-id="29385-129">-Confirm</span></span>
<span data-ttu-id="29385-130">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="29385-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="29385-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="29385-131">-WhatIf</span></span>
<span data-ttu-id="29385-132">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="29385-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="29385-133">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="29385-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="29385-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29385-134">CommonParameters</span></span>
<span data-ttu-id="29385-135">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="29385-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="29385-136">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="29385-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29385-137">輸入</span><span class="sxs-lookup"><span data-stu-id="29385-137">INPUTS</span></span>

### <span data-ttu-id="29385-138">System.object</span><span class="sxs-lookup"><span data-stu-id="29385-138">System.String</span></span>
<span data-ttu-id="29385-139">PSHybridConnectionAttibutes System. Null ' 1 @ [System.object，mscorlib，版本 = 4.0.0.0，Culture = 中立，PublicKeyToken = b77a5c561934e089]]。</span><span class="sxs-lookup"><span data-stu-id="29385-139">Microsoft.Azure.Commands.Relay.Models.PSHybridConnectionAttibutes System.Nullable\`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>


## <span data-ttu-id="29385-140">輸出</span><span class="sxs-lookup"><span data-stu-id="29385-140">OUTPUTS</span></span>

### <span data-ttu-id="29385-141">PSHybridConnectionAttibutes 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="29385-141">Microsoft.Azure.Commands.Relay.Models.PSHybridConnectionAttibutes</span></span>


## <span data-ttu-id="29385-142">筆記</span><span class="sxs-lookup"><span data-stu-id="29385-142">NOTES</span></span>

## <span data-ttu-id="29385-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="29385-143">RELATED LINKS</span></span>
