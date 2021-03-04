---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/powershell/module/az.servicebus/remove-azservicebusnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusNamespace.md
ms.openlocfilehash: 7f6a7225742356e0410d3cc49aef60e50e1954a6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101908449"
---
# <span data-ttu-id="de54f-101">Remove-AzServiceBusNamespace</span><span class="sxs-lookup"><span data-stu-id="de54f-101">Remove-AzServiceBusNamespace</span></span>

## <span data-ttu-id="de54f-102">簡介</span><span class="sxs-lookup"><span data-stu-id="de54f-102">SYNOPSIS</span></span>
<span data-ttu-id="de54f-103">從指定的資源群組移除命名空間。</span><span class="sxs-lookup"><span data-stu-id="de54f-103">Removes the namespace from the specified resource group.</span></span> 

## <span data-ttu-id="de54f-104">語法</span><span class="sxs-lookup"><span data-stu-id="de54f-104">SYNTAX</span></span>

### <span data-ttu-id="de54f-105">命名空間PropertiesSet (預設) </span><span class="sxs-lookup"><span data-stu-id="de54f-105">NamespacePropertiesSet (Default)</span></span>
```
Remove-AzServiceBusNamespace [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="de54f-106">命名空間InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="de54f-106">NamespaceInputObjectSet</span></span>
```
Remove-AzServiceBusNamespace [-InputObject] <PSNamespaceAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="de54f-107">命名空間ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="de54f-107">NamespaceResourceIdParameterSet</span></span>
```
Remove-AzServiceBusNamespace [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="de54f-108">描述</span><span class="sxs-lookup"><span data-stu-id="de54f-108">DESCRIPTION</span></span>
<span data-ttu-id="de54f-109">**Remove-AzServiceBusNamespace** Cmdlet 會從指定的資源群組移除命名空間。</span><span class="sxs-lookup"><span data-stu-id="de54f-109">The **Remove-AzServiceBusNamespace** cmdlet removes the namespace from the specified resource group.</span></span>

## <span data-ttu-id="de54f-110">例子</span><span class="sxs-lookup"><span data-stu-id="de54f-110">EXAMPLES</span></span>

### <span data-ttu-id="de54f-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="de54f-111">Example 1</span></span>
```
PS C:\> Remove-AzServiceBusNamespace -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1
```

<span data-ttu-id="de54f-112">從指定的資源群組移除 Service Bus `SB-Example1` 命名空間 `Default-ServiceBus-WestUS` 。</span><span class="sxs-lookup"><span data-stu-id="de54f-112">Removes the Service Bus namespace `SB-Example1` from the specified resource group `Default-ServiceBus-WestUS`.</span></span>

### <span data-ttu-id="de54f-113">範例 2.1 - InputObject - Using variable：</span><span class="sxs-lookup"><span data-stu-id="de54f-113">Example 2.1 - InputObject - Using variable:</span></span>
```
PS C:\> $inputobject = Get-AzServiceBusNamespace <params>
PS C:\> Remove-AzServiceBusNamespace -InputObject $inputobject
```

<span data-ttu-id="de54f-114">移除透過此資料夾提供的 Service Bus 命名空間$inputobject。</span><span class="sxs-lookup"><span data-stu-id="de54f-114">Removes the Service Bus namespace provided through the $inputobject.</span></span>

### <span data-ttu-id="de54f-115">範例 2.2 - InputObject - 使用管道：</span><span class="sxs-lookup"><span data-stu-id="de54f-115">Example 2.2 - InputObject - Using Piping:</span></span>
```
PS C:\> Get-AzServiceBusNamespace <params> | Remove-AzServiceBusNamespace
```

<span data-ttu-id="de54f-116">使用管道移除 Service Bus 命名空間。</span><span class="sxs-lookup"><span data-stu-id="de54f-116">Removes the Service Bus namespace using Piping.</span></span>

### <span data-ttu-id="de54f-117">範例 3 - ResourceId</span><span class="sxs-lookup"><span data-stu-id="de54f-117">Example 3 - ResourceId</span></span>
```
PS c:\> $ResourceId = (Get-AzResource -ResourceType Microsoft.ServiceBus/namespaces).ResourceId
PS C:\> Remove-AzServiceBusNamespace -ResourceId $resourceid
```

<span data-ttu-id="de54f-118">移除透過 ARM 識別碼在 $resourceid ResourceId 參數或管道中提供的 Service Bus 命名空間。</span><span class="sxs-lookup"><span data-stu-id="de54f-118">Removes the Service Bus namespace provided through ARM id in $resourceid for -ResourceId parameter or through piping.</span></span>

## <span data-ttu-id="de54f-119">參數</span><span class="sxs-lookup"><span data-stu-id="de54f-119">PARAMETERS</span></span>

### <span data-ttu-id="de54f-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="de54f-120">-AsJob</span></span>
<span data-ttu-id="de54f-121">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="de54f-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="de54f-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de54f-122">-DefaultProfile</span></span>
<span data-ttu-id="de54f-123">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="de54f-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="de54f-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="de54f-124">-InputObject</span></span>
<span data-ttu-id="de54f-125">Service Bus 命名空間物件</span><span class="sxs-lookup"><span data-stu-id="de54f-125">Service Bus Namespace Object</span></span>

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

### <span data-ttu-id="de54f-126">-名稱</span><span class="sxs-lookup"><span data-stu-id="de54f-126">-Name</span></span>
<span data-ttu-id="de54f-127">命名空間名稱。</span><span class="sxs-lookup"><span data-stu-id="de54f-127">Namespace Name.</span></span>

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

### <span data-ttu-id="de54f-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="de54f-128">-PassThru</span></span>
<span data-ttu-id="de54f-129">如果命令成功，指定此選項會返回 True。</span><span class="sxs-lookup"><span data-stu-id="de54f-129">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="de54f-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="de54f-130">-ResourceGroupName</span></span>
<span data-ttu-id="de54f-131">資源組的名稱</span><span class="sxs-lookup"><span data-stu-id="de54f-131">The name of the resource group</span></span>

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

### <span data-ttu-id="de54f-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="de54f-132">-ResourceId</span></span>
<span data-ttu-id="de54f-133">服務母線命名空間資源識別碼</span><span class="sxs-lookup"><span data-stu-id="de54f-133">Service Bus Namespace Resource Id</span></span>

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

### <span data-ttu-id="de54f-134">-確認</span><span class="sxs-lookup"><span data-stu-id="de54f-134">-Confirm</span></span>
<span data-ttu-id="de54f-135">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="de54f-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="de54f-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="de54f-136">-WhatIf</span></span>
<span data-ttu-id="de54f-137">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="de54f-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="de54f-138">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="de54f-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="de54f-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de54f-139">CommonParameters</span></span>
<span data-ttu-id="de54f-140">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="de54f-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de54f-141">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="de54f-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de54f-142">輸入</span><span class="sxs-lookup"><span data-stu-id="de54f-142">INPUTS</span></span>

### <span data-ttu-id="de54f-143">System.String</span><span class="sxs-lookup"><span data-stu-id="de54f-143">System.String</span></span>

### <span data-ttu-id="de54f-144">Microsoft.Azure.Commands.ServiceBus.models.PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="de54f-144">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="de54f-145">輸出</span><span class="sxs-lookup"><span data-stu-id="de54f-145">OUTPUTS</span></span>

### <span data-ttu-id="de54f-146">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="de54f-146">System.Boolean</span></span>

## <span data-ttu-id="de54f-147">筆記</span><span class="sxs-lookup"><span data-stu-id="de54f-147">NOTES</span></span>

## <span data-ttu-id="de54f-148">相關連結</span><span class="sxs-lookup"><span data-stu-id="de54f-148">RELATED LINKS</span></span>
