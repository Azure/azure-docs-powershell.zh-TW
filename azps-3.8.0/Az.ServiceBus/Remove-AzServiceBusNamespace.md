---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/remove-azservicebusnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusNamespace.md
ms.openlocfilehash: 49b6a29410bd6c670e74b072a48b6f2a79e8fd0f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93957236"
---
# <span data-ttu-id="02aee-101">Remove-AzServiceBusNamespace</span><span class="sxs-lookup"><span data-stu-id="02aee-101">Remove-AzServiceBusNamespace</span></span>

## <span data-ttu-id="02aee-102">摘要</span><span class="sxs-lookup"><span data-stu-id="02aee-102">SYNOPSIS</span></span>
<span data-ttu-id="02aee-103">從指定的資源群組中移除命名空間。</span><span class="sxs-lookup"><span data-stu-id="02aee-103">Removes the namespace from the specified resource group.</span></span> 

## <span data-ttu-id="02aee-104">句法</span><span class="sxs-lookup"><span data-stu-id="02aee-104">SYNTAX</span></span>

### <span data-ttu-id="02aee-105">NamespacePropertiesSet (預設) </span><span class="sxs-lookup"><span data-stu-id="02aee-105">NamespacePropertiesSet (Default)</span></span>
```
Remove-AzServiceBusNamespace [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="02aee-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="02aee-106">NamespaceInputObjectSet</span></span>
```
Remove-AzServiceBusNamespace [-InputObject] <PSNamespaceAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="02aee-107">NamespaceResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="02aee-107">NamespaceResourceIdParameterSet</span></span>
```
Remove-AzServiceBusNamespace [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="02aee-108">說明</span><span class="sxs-lookup"><span data-stu-id="02aee-108">DESCRIPTION</span></span>
<span data-ttu-id="02aee-109">**AzServiceBusNamespace** Cmdlet 會從指定的資源群組中移除命名空間。</span><span class="sxs-lookup"><span data-stu-id="02aee-109">The **Remove-AzServiceBusNamespace** cmdlet removes the namespace from the specified resource group.</span></span>

## <span data-ttu-id="02aee-110">示例</span><span class="sxs-lookup"><span data-stu-id="02aee-110">EXAMPLES</span></span>

### <span data-ttu-id="02aee-111">範例1</span><span class="sxs-lookup"><span data-stu-id="02aee-111">Example 1</span></span>
```
PS C:\> Remove-AzServiceBusNamespace -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1
```

<span data-ttu-id="02aee-112">`SB-Example1`從指定的資源群組中移除服務匯流排命名空間 `Default-ServiceBus-WestUS` 。</span><span class="sxs-lookup"><span data-stu-id="02aee-112">Removes the Service Bus namespace `SB-Example1` from the specified resource group `Default-ServiceBus-WestUS`.</span></span>

### <span data-ttu-id="02aee-113">範例 2.1-使用變數：</span><span class="sxs-lookup"><span data-stu-id="02aee-113">Example 2.1 - InputObject - Using variable:</span></span>
```
PS C:\> $inputobject = Get-AzServiceBusNamespace <params>
PS C:\> Remove-AzServiceBusNamespace -InputObject $inputobject
```

<span data-ttu-id="02aee-114">移除透過 $inputobject 提供的服務匯流排命名空間。</span><span class="sxs-lookup"><span data-stu-id="02aee-114">Removes the Service Bus namespace provided through the $inputobject.</span></span>

### <span data-ttu-id="02aee-115">範例 2.2-使用管道的 InputObject：</span><span class="sxs-lookup"><span data-stu-id="02aee-115">Example 2.2 - InputObject - Using Piping:</span></span>
```
PS C:\> Get-AzServiceBusNamespace <params> | Remove-AzServiceBusNamespace
```

<span data-ttu-id="02aee-116">使用 [管道] 移除服務匯流排命名空間。</span><span class="sxs-lookup"><span data-stu-id="02aee-116">Removes the Service Bus namespace using Piping.</span></span>

### <span data-ttu-id="02aee-117">範例 3-ResourceId</span><span class="sxs-lookup"><span data-stu-id="02aee-117">Example 3 - ResourceId</span></span>
```
PS c:\> $ResourceId = (Get-AzResource -ResourceType Microsoft.ServiceBus/namespaces).ResourceId
PS C:\> Remove-AzServiceBusNamespace -ResourceId $resourceid
```

<span data-ttu-id="02aee-118">移除透過 ARM 識別碼提供的服務匯流排命名空間，在 $resourceid 中，或透過管道。</span><span class="sxs-lookup"><span data-stu-id="02aee-118">Removes the Service Bus namespace provided through ARM id in $resourceid for -ResourceId parameter or through piping.</span></span>

## <span data-ttu-id="02aee-119">參數</span><span class="sxs-lookup"><span data-stu-id="02aee-119">PARAMETERS</span></span>

### <span data-ttu-id="02aee-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="02aee-120">-AsJob</span></span>
<span data-ttu-id="02aee-121">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="02aee-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="02aee-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02aee-122">-DefaultProfile</span></span>
<span data-ttu-id="02aee-123">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="02aee-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="02aee-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="02aee-124">-InputObject</span></span>
<span data-ttu-id="02aee-125">服務匯流排命名空間物件</span><span class="sxs-lookup"><span data-stu-id="02aee-125">Service Bus Namespace Object</span></span>

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

### <span data-ttu-id="02aee-126">-名稱</span><span class="sxs-lookup"><span data-stu-id="02aee-126">-Name</span></span>
<span data-ttu-id="02aee-127">命名空間名稱。</span><span class="sxs-lookup"><span data-stu-id="02aee-127">Namespace Name.</span></span>

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

### <span data-ttu-id="02aee-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="02aee-128">-PassThru</span></span>
<span data-ttu-id="02aee-129">如果命令成功，則指定此值會傳回 true。</span><span class="sxs-lookup"><span data-stu-id="02aee-129">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="02aee-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="02aee-130">-ResourceGroupName</span></span>
<span data-ttu-id="02aee-131">資源群組的名稱</span><span class="sxs-lookup"><span data-stu-id="02aee-131">The name of the resource group</span></span>

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

### <span data-ttu-id="02aee-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="02aee-132">-ResourceId</span></span>
<span data-ttu-id="02aee-133">服務匯流排命名空間資源識別碼</span><span class="sxs-lookup"><span data-stu-id="02aee-133">Service Bus Namespace Resource Id</span></span>

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

### <span data-ttu-id="02aee-134">-確認</span><span class="sxs-lookup"><span data-stu-id="02aee-134">-Confirm</span></span>
<span data-ttu-id="02aee-135">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="02aee-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="02aee-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="02aee-136">-WhatIf</span></span>
<span data-ttu-id="02aee-137">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="02aee-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="02aee-138">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="02aee-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="02aee-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02aee-139">CommonParameters</span></span>
<span data-ttu-id="02aee-140">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="02aee-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02aee-141">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="02aee-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02aee-142">輸入</span><span class="sxs-lookup"><span data-stu-id="02aee-142">INPUTS</span></span>

### <span data-ttu-id="02aee-143">System.object</span><span class="sxs-lookup"><span data-stu-id="02aee-143">System.String</span></span>

### <span data-ttu-id="02aee-144">PSNamespaceAttributes 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="02aee-144">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="02aee-145">輸出</span><span class="sxs-lookup"><span data-stu-id="02aee-145">OUTPUTS</span></span>

### <span data-ttu-id="02aee-146">System.object</span><span class="sxs-lookup"><span data-stu-id="02aee-146">System.Boolean</span></span>

## <span data-ttu-id="02aee-147">筆記</span><span class="sxs-lookup"><span data-stu-id="02aee-147">NOTES</span></span>

## <span data-ttu-id="02aee-148">相關連結</span><span class="sxs-lookup"><span data-stu-id="02aee-148">RELATED LINKS</span></span>