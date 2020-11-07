---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/remove-azurermservicebusnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusNamespace.md
ms.openlocfilehash: c56637b8470e40e6b46984117a764da248684005
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93623893"
---
# <span data-ttu-id="1dd49-101">Remove-AzureRmServiceBusNamespace</span><span class="sxs-lookup"><span data-stu-id="1dd49-101">Remove-AzureRmServiceBusNamespace</span></span>

## <span data-ttu-id="1dd49-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1dd49-102">SYNOPSIS</span></span>
<span data-ttu-id="1dd49-103">從指定的資源群組中移除命名空間。</span><span class="sxs-lookup"><span data-stu-id="1dd49-103">Removes the namespace from the specified resource group.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1dd49-104">句法</span><span class="sxs-lookup"><span data-stu-id="1dd49-104">SYNTAX</span></span>

### <span data-ttu-id="1dd49-105">NamespacePropertiesSet (預設) </span><span class="sxs-lookup"><span data-stu-id="1dd49-105">NamespacePropertiesSet (Default)</span></span>
```
Remove-AzureRmServiceBusNamespace [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1dd49-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="1dd49-106">NamespaceInputObjectSet</span></span>
```
Remove-AzureRmServiceBusNamespace [-InputObject] <PSNamespaceAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1dd49-107">NamespaceResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1dd49-107">NamespaceResourceIdParameterSet</span></span>
```
Remove-AzureRmServiceBusNamespace [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1dd49-108">說明</span><span class="sxs-lookup"><span data-stu-id="1dd49-108">DESCRIPTION</span></span>
<span data-ttu-id="1dd49-109">**AzureRmServiceBusNamespace** Cmdlet 會從指定的資源群組中移除命名空間。</span><span class="sxs-lookup"><span data-stu-id="1dd49-109">The **Remove-AzureRmServiceBusNamespace** cmdlet removes the namespace from the specified resource group.</span></span>

## <span data-ttu-id="1dd49-110">示例</span><span class="sxs-lookup"><span data-stu-id="1dd49-110">EXAMPLES</span></span>

### <span data-ttu-id="1dd49-111">範例1</span><span class="sxs-lookup"><span data-stu-id="1dd49-111">Example 1</span></span>
```
PS C:\> Remove-AzureRmServiceBusNamespace -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1
```

<span data-ttu-id="1dd49-112">`SB-Example1`從指定的資源群組中移除服務匯流排命名空間 `Default-ServiceBus-WestUS` 。</span><span class="sxs-lookup"><span data-stu-id="1dd49-112">Removes the Service Bus namespace `SB-Example1` from the specified resource group `Default-ServiceBus-WestUS`.</span></span>

### <span data-ttu-id="1dd49-113">範例 2.1-使用變數：</span><span class="sxs-lookup"><span data-stu-id="1dd49-113">Example 2.1 - InputObject - Using variable:</span></span>
```
PS C:\> $inputobject = Get-AzureRmServiceBusNamespace <params>
PS C:\> Remove-AzureRmServiceBusNamespace -InputObject $inputobject
```

<span data-ttu-id="1dd49-114">移除透過 $inputobject 提供的服務匯流排命名空間。</span><span class="sxs-lookup"><span data-stu-id="1dd49-114">Removes the Service Bus namespace provided through the $inputobject.</span></span>

### <span data-ttu-id="1dd49-115">範例 2.2-使用管道的 InputObject：</span><span class="sxs-lookup"><span data-stu-id="1dd49-115">Example 2.2 - InputObject - Using Piping:</span></span>
```
PS C:\> Get-AzureRmServiceBusNamespace <params> | Remove-AzureRmServiceBusNamespace
```

<span data-ttu-id="1dd49-116">使用 [管道] 移除服務匯流排命名空間。</span><span class="sxs-lookup"><span data-stu-id="1dd49-116">Removes the Service Bus namespace using Piping.</span></span>

### <span data-ttu-id="1dd49-117">範例 3-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1dd49-117">Example 3 - ResourceId</span></span>
```
PS c:\> $ResourceId = (Get-AzureRmResource -ResourceType Microsoft.ServiceBus/namespaces).ResourceId
PS C:\> Remove-AzureRmServiceBusNamespace -ResourceId $resourceid
```

<span data-ttu-id="1dd49-118">移除透過 ARM 識別碼提供的服務匯流排命名空間，在 $resourceid 中，或透過管道。</span><span class="sxs-lookup"><span data-stu-id="1dd49-118">Removes the Service Bus namespace provided through ARM id in $resourceid for -ResourceId parameter or through piping.</span></span>

## <span data-ttu-id="1dd49-119">參數</span><span class="sxs-lookup"><span data-stu-id="1dd49-119">PARAMETERS</span></span>

### <span data-ttu-id="1dd49-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1dd49-120">-AsJob</span></span>
<span data-ttu-id="1dd49-121">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="1dd49-121">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1dd49-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1dd49-122">-DefaultProfile</span></span>
<span data-ttu-id="1dd49-123">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="1dd49-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1dd49-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1dd49-124">-InputObject</span></span>
<span data-ttu-id="1dd49-125">服務匯流排命名空間物件</span><span class="sxs-lookup"><span data-stu-id="1dd49-125">Service Bus Namespace Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes
Parameter Sets: NamespaceInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1dd49-126">-名稱</span><span class="sxs-lookup"><span data-stu-id="1dd49-126">-Name</span></span>
<span data-ttu-id="1dd49-127">命名空間名稱。</span><span class="sxs-lookup"><span data-stu-id="1dd49-127">Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NamespacePropertiesSet
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1dd49-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1dd49-128">-PassThru</span></span>
<span data-ttu-id="1dd49-129">如果命令成功，則指定此值會傳回 true。</span><span class="sxs-lookup"><span data-stu-id="1dd49-129">Specifying this will return true if the command was successful.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1dd49-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1dd49-130">-ResourceGroupName</span></span>
<span data-ttu-id="1dd49-131">資源群組的名稱</span><span class="sxs-lookup"><span data-stu-id="1dd49-131">The name of the resource group</span></span>

```yaml
Type: System.String
Parameter Sets: NamespacePropertiesSet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1dd49-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1dd49-132">-ResourceId</span></span>
<span data-ttu-id="1dd49-133">服務匯流排命名空間資源識別碼</span><span class="sxs-lookup"><span data-stu-id="1dd49-133">Service Bus Namespace Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: NamespaceResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1dd49-134">-確認</span><span class="sxs-lookup"><span data-stu-id="1dd49-134">-Confirm</span></span>
<span data-ttu-id="1dd49-135">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="1dd49-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1dd49-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1dd49-136">-WhatIf</span></span>
<span data-ttu-id="1dd49-137">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="1dd49-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1dd49-138">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1dd49-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1dd49-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1dd49-139">CommonParameters</span></span>
<span data-ttu-id="1dd49-140">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1dd49-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1dd49-141">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="1dd49-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1dd49-142">輸入</span><span class="sxs-lookup"><span data-stu-id="1dd49-142">INPUTS</span></span>

### <span data-ttu-id="1dd49-143">System.object</span><span class="sxs-lookup"><span data-stu-id="1dd49-143">System.String</span></span>

### <span data-ttu-id="1dd49-144">PSNamespaceAttributes 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="1dd49-144">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span></span>
<span data-ttu-id="1dd49-145">參數： InputObject (ByValue) </span><span class="sxs-lookup"><span data-stu-id="1dd49-145">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="1dd49-146">輸出</span><span class="sxs-lookup"><span data-stu-id="1dd49-146">OUTPUTS</span></span>

### <span data-ttu-id="1dd49-147">System.object</span><span class="sxs-lookup"><span data-stu-id="1dd49-147">System.Boolean</span></span>

## <span data-ttu-id="1dd49-148">筆記</span><span class="sxs-lookup"><span data-stu-id="1dd49-148">NOTES</span></span>

## <span data-ttu-id="1dd49-149">相關連結</span><span class="sxs-lookup"><span data-stu-id="1dd49-149">RELATED LINKS</span></span>
