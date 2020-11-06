---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/set-azurermservicebusgeodrconfigurationbreakpair
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusGeoDRConfigurationBreakPair.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusGeoDRConfigurationBreakPair.md
ms.openlocfilehash: a12f22260ce8ee5412cd17ddfa420a7d23f82008
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448905"
---
# <span data-ttu-id="1919e-101">Set-AzureRmServiceBusGeoDRConfigurationBreakPair</span><span class="sxs-lookup"><span data-stu-id="1919e-101">Set-AzureRmServiceBusGeoDRConfigurationBreakPair</span></span>

## <span data-ttu-id="1919e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1919e-102">SYNOPSIS</span></span>
<span data-ttu-id="1919e-103">這個作業會停用災害復原，並停止將主要的變更複製到次要命名空間</span><span class="sxs-lookup"><span data-stu-id="1919e-103">This operation disables the Disaster Recovery and stops replicating changes from primary to secondary namespaces</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1919e-104">句法</span><span class="sxs-lookup"><span data-stu-id="1919e-104">SYNTAX</span></span>

### <span data-ttu-id="1919e-105">GeoDRPropertiesSet (預設) </span><span class="sxs-lookup"><span data-stu-id="1919e-105">GeoDRPropertiesSet (Default)</span></span>
```
Set-AzureRmServiceBusGeoDRConfigurationBreakPair [-ResourceGroupName] <String> [-Namespace] <String>
 [-Name] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1919e-106">GeoDRConfigurationInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="1919e-106">GeoDRConfigurationInputObjectSet</span></span>
```
Set-AzureRmServiceBusGeoDRConfigurationBreakPair [-InputObject] <PSServiceBusDRConfigurationAttributes>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1919e-107">GeoDRConfigResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1919e-107">GeoDRConfigResourceIdParameterSet</span></span>
```
Set-AzureRmServiceBusGeoDRConfigurationBreakPair [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1919e-108">說明</span><span class="sxs-lookup"><span data-stu-id="1919e-108">DESCRIPTION</span></span>
<span data-ttu-id="1919e-109">**AzureRmServiceBusGeoDRConfigurationBreakPair** Cmdlet 會停用災害復原，並停止將主要的變更複製到次要命名空間</span><span class="sxs-lookup"><span data-stu-id="1919e-109">The **Set-AzureRmServiceBusGeoDRConfigurationBreakPair** cmdlet disables the Disaster Recovery and stops replicating changes from primary to secondary namespaces</span></span>

## <span data-ttu-id="1919e-110">示例</span><span class="sxs-lookup"><span data-stu-id="1919e-110">EXAMPLES</span></span>

### <span data-ttu-id="1919e-111">範例1</span><span class="sxs-lookup"><span data-stu-id="1919e-111">Example 1</span></span>
```
PS C:\> Set-AzureRmServiceBusGeoDRConfigurationBreakPair -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Primary" -Name "SampleDRCongifName"
```

<span data-ttu-id="1919e-112">這個作業會停用災害復原，並停止將主要的變更複製到次要命名空間</span><span class="sxs-lookup"><span data-stu-id="1919e-112">This operation disables the Disaster Recovery and stops replicating changes from primary to secondary namespaces</span></span>

## <span data-ttu-id="1919e-113">參數</span><span class="sxs-lookup"><span data-stu-id="1919e-113">PARAMETERS</span></span>

### <span data-ttu-id="1919e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1919e-114">-DefaultProfile</span></span>
<span data-ttu-id="1919e-115">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="1919e-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1919e-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1919e-116">-InputObject</span></span>
<span data-ttu-id="1919e-117">服務匯流排 GeoDR 設定物件</span><span class="sxs-lookup"><span data-stu-id="1919e-117">Service Bus GeoDR Configuration Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes
Parameter Sets: GeoDRConfigurationInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1919e-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="1919e-118">-Name</span></span>
<span data-ttu-id="1919e-119">DR 配置名稱</span><span class="sxs-lookup"><span data-stu-id="1919e-119">DR Configuration Name</span></span>

```yaml
Type: System.String
Parameter Sets: GeoDRPropertiesSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1919e-120">-命名空間</span><span class="sxs-lookup"><span data-stu-id="1919e-120">-Namespace</span></span>
<span data-ttu-id="1919e-121">命名空間名稱-主要命名空間</span><span class="sxs-lookup"><span data-stu-id="1919e-121">Namespace Name - Primary Namespace</span></span>

```yaml
Type: System.String
Parameter Sets: GeoDRPropertiesSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1919e-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1919e-122">-PassThru</span></span>
<span data-ttu-id="1919e-123">傳回代表您正在使用之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="1919e-123">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="1919e-124">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="1919e-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="1919e-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1919e-125">-ResourceGroupName</span></span>
<span data-ttu-id="1919e-126">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="1919e-126">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: GeoDRPropertiesSet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1919e-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1919e-127">-ResourceId</span></span>
<span data-ttu-id="1919e-128">GeoDRConfiguration 資源識別碼</span><span class="sxs-lookup"><span data-stu-id="1919e-128">GeoDRConfiguration Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: GeoDRConfigResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1919e-129">-確認</span><span class="sxs-lookup"><span data-stu-id="1919e-129">-Confirm</span></span>
<span data-ttu-id="1919e-130">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="1919e-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1919e-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1919e-131">-WhatIf</span></span>
<span data-ttu-id="1919e-132">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="1919e-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1919e-133">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1919e-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1919e-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1919e-134">CommonParameters</span></span>
<span data-ttu-id="1919e-135">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1919e-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1919e-136">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="1919e-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1919e-137">輸入</span><span class="sxs-lookup"><span data-stu-id="1919e-137">INPUTS</span></span>

### <span data-ttu-id="1919e-138">System.object</span><span class="sxs-lookup"><span data-stu-id="1919e-138">System.String</span></span>

### <span data-ttu-id="1919e-139">PSServiceBusDRConfigurationAttributes 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="1919e-139">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>
<span data-ttu-id="1919e-140">參數： InputObject (ByValue) </span><span class="sxs-lookup"><span data-stu-id="1919e-140">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="1919e-141">輸出</span><span class="sxs-lookup"><span data-stu-id="1919e-141">OUTPUTS</span></span>

### <span data-ttu-id="1919e-142">System.object</span><span class="sxs-lookup"><span data-stu-id="1919e-142">System.Boolean</span></span>

## <span data-ttu-id="1919e-143">筆記</span><span class="sxs-lookup"><span data-stu-id="1919e-143">NOTES</span></span>

## <span data-ttu-id="1919e-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="1919e-144">RELATED LINKS</span></span>
