---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusNamespaceKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusNamespaceKey.md
ms.openlocfilehash: 5b366a3be8ca715a42c1c1f916d8ebf327dff8fc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93452348"
---
# <span data-ttu-id="e8568-101">New-AzureRmServiceBusNamespaceKey</span><span class="sxs-lookup"><span data-stu-id="e8568-101">New-AzureRmServiceBusNamespaceKey</span></span>

## <span data-ttu-id="e8568-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e8568-102">SYNOPSIS</span></span>
<span data-ttu-id="e8568-103">重新產生服務匯流排命名空間的主要或次要連接字串。</span><span class="sxs-lookup"><span data-stu-id="e8568-103">Regenerates the primary or secondary connection strings for the Service Bus namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e8568-104">句法</span><span class="sxs-lookup"><span data-stu-id="e8568-104">SYNTAX</span></span>

```
New-AzureRmServiceBusNamespaceKey [-ResourceGroup] <String> -Namespace <String> -Name <String>
 [-RegenerateKeys] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e8568-105">說明</span><span class="sxs-lookup"><span data-stu-id="e8568-105">DESCRIPTION</span></span>
<span data-ttu-id="e8568-106">**新的-AzureRmServiceBusNamespace** Cmdlet 會針對指定的命名空間和授權規則產生新的主要或次要連接字串。</span><span class="sxs-lookup"><span data-stu-id="e8568-106">The **New-AzureRmServiceBusNamespace** cmdlet generates new primary or secondary connection strings for the specified namespace and authorization rule.</span></span>

## <span data-ttu-id="e8568-107">示例</span><span class="sxs-lookup"><span data-stu-id="e8568-107">EXAMPLES</span></span>

### <span data-ttu-id="e8568-108">範例1</span><span class="sxs-lookup"><span data-stu-id="e8568-108">Example 1</span></span>
```
PS C:\> New-AzureRmServiceBusNamespaceKey -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -AuthorizationRuleName AuthoRule1 -RegenerateKeys PrimaryKey
```

<span data-ttu-id="e8568-109">重新生成命名空間的主要或次要連接字串。</span><span class="sxs-lookup"><span data-stu-id="e8568-109">Regenerates the primary or secondary connection strings for the namespace.</span></span>

## <span data-ttu-id="e8568-110">參數</span><span class="sxs-lookup"><span data-stu-id="e8568-110">PARAMETERS</span></span>

### <span data-ttu-id="e8568-111">-RegenerateKeys</span><span class="sxs-lookup"><span data-stu-id="e8568-111">-RegenerateKeys</span></span>
<span data-ttu-id="e8568-112">重新產生金鑰： PrimaryKey/SecondaryKey。</span><span class="sxs-lookup"><span data-stu-id="e8568-112">Regenerate Keys: PrimaryKey/SecondaryKey.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: PrimaryKey, SecondaryKey

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8568-113">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="e8568-113">-ResourceGroup</span></span>
<span data-ttu-id="e8568-114">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="e8568-114">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroupName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8568-115">-確認</span><span class="sxs-lookup"><span data-stu-id="e8568-115">-Confirm</span></span>
<span data-ttu-id="e8568-116">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="e8568-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e8568-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e8568-117">-WhatIf</span></span>
<span data-ttu-id="e8568-118">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="e8568-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e8568-119">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e8568-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e8568-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8568-120">-DefaultProfile</span></span>
<span data-ttu-id="e8568-121">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e8568-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e8568-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="e8568-122">-Name</span></span>
<span data-ttu-id="e8568-123">授權規則名稱。</span><span class="sxs-lookup"><span data-stu-id="e8568-123">Authorization Rule Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8568-124">-命名空間</span><span class="sxs-lookup"><span data-stu-id="e8568-124">-Namespace</span></span>
<span data-ttu-id="e8568-125">命名空間名稱。</span><span class="sxs-lookup"><span data-stu-id="e8568-125">Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8568-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8568-126">CommonParameters</span></span>
<span data-ttu-id="e8568-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e8568-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8568-128">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="e8568-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8568-129">輸入</span><span class="sxs-lookup"><span data-stu-id="e8568-129">INPUTS</span></span>

### <span data-ttu-id="e8568-130">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="e8568-130">-ResourceGroup</span></span>
 <span data-ttu-id="e8568-131">System.object</span><span class="sxs-lookup"><span data-stu-id="e8568-131">System.String</span></span>
 

### <span data-ttu-id="e8568-132">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="e8568-132">-NamespaceName</span></span>
 <span data-ttu-id="e8568-133">System.object</span><span class="sxs-lookup"><span data-stu-id="e8568-133">System.String</span></span>
 

### <span data-ttu-id="e8568-134">-AuthorizationRuleName</span><span class="sxs-lookup"><span data-stu-id="e8568-134">-AuthorizationRuleName</span></span>
 <span data-ttu-id="e8568-135">System.object</span><span class="sxs-lookup"><span data-stu-id="e8568-135">System.String</span></span>
 

### <span data-ttu-id="e8568-136">-RegenerateKeys</span><span class="sxs-lookup"><span data-stu-id="e8568-136">-RegenerateKeys</span></span>
 <span data-ttu-id="e8568-137">System.object</span><span class="sxs-lookup"><span data-stu-id="e8568-137">System.String</span></span>

## <span data-ttu-id="e8568-138">輸出</span><span class="sxs-lookup"><span data-stu-id="e8568-138">OUTPUTS</span></span>

### <span data-ttu-id="e8568-139">ResourceListKeys （即 Azure。</span><span class="sxs-lookup"><span data-stu-id="e8568-139">Microsoft.Azure.Management.ServiceBus.Models.ResourceListKeys</span></span>
<span data-ttu-id="e8568-140">PrimaryConnectionString： Endpoint = sb：//sb-example1.servicebus.windows.net/;SharedAccessKeyName = AuthoRule1;SharedAccessKey = {SharedAccessKey 值} SecondaryConnectionString： Endpoint = sb：//sb-example1.servicebus.windows.net/;SharedAccessKeyName = AuthoRule1;SharedAccessKey = {SharedAccessKey 值} PrimaryKey： {PrimaryKey 值} SecondaryKey： {SecondaryKey 值} KeyName： AuthoRule1</span><span class="sxs-lookup"><span data-stu-id="e8568-140">PrimaryConnectionString   : Endpoint=sb://sb-example1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey={SharedAccessKey-value} SecondaryConnectionString : Endpoint=sb://sb-example1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey={SharedAccessKey-value} PrimaryKey                : {PrimaryKey value} SecondaryKey              : {SecondaryKey value} KeyName                   : AuthoRule1</span></span>

## <span data-ttu-id="e8568-141">筆記</span><span class="sxs-lookup"><span data-stu-id="e8568-141">NOTES</span></span>

## <span data-ttu-id="e8568-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="e8568-142">RELATED LINKS</span></span>

