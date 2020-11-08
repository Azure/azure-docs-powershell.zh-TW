---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/set-azeventhubgeodrconfigurationfailover
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubGeoDRConfigurationFailOver.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubGeoDRConfigurationFailOver.md
ms.openlocfilehash: 4ee96fbe20fca3f0af1f0bb9604f178b912d0ea2
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "93969729"
---
# <span data-ttu-id="e375a-101">Set-AzEventHubGeoDRConfigurationFailOver</span><span class="sxs-lookup"><span data-stu-id="e375a-101">Set-AzEventHubGeoDRConfigurationFailOver</span></span>

## <span data-ttu-id="e375a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e375a-102">SYNOPSIS</span></span>
<span data-ttu-id="e375a-103">調用 GEO DR 容錯移轉，並重新設定別名以指向次要命名空間</span><span class="sxs-lookup"><span data-stu-id="e375a-103">Invokes GEO DR failover and reconfigure the alias to point to the secondary namespace</span></span>

## <span data-ttu-id="e375a-104">句法</span><span class="sxs-lookup"><span data-stu-id="e375a-104">SYNTAX</span></span>

### <span data-ttu-id="e375a-105">GeoDRParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="e375a-105">GeoDRParameterSet (Default)</span></span>
```
Set-AzEventHubGeoDRConfigurationFailOver [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e375a-106">GeoDRConfigurationInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="e375a-106">GeoDRConfigurationInputObjectSet</span></span>
```
Set-AzEventHubGeoDRConfigurationFailOver [-InputObject] <PSEventHubDRConfigurationAttributes> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e375a-107">GeoDRConfigResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e375a-107">GeoDRConfigResourceIdParameterSet</span></span>
```
Set-AzEventHubGeoDRConfigurationFailOver [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e375a-108">說明</span><span class="sxs-lookup"><span data-stu-id="e375a-108">DESCRIPTION</span></span>
<span data-ttu-id="e375a-109">AzEventHubGeoDRConfigurationFailOver Cmdlet 會調用 GEO DR 容錯移轉，並 **將** 別名重新設定為指向次要命名空間</span><span class="sxs-lookup"><span data-stu-id="e375a-109">The **Set-AzEventHubGeoDRConfigurationFailOver** cmdlet invokes GEO DR failover and reconfigure the alias to point to the secondary namespace</span></span>

## <span data-ttu-id="e375a-110">示例</span><span class="sxs-lookup"><span data-stu-id="e375a-110">EXAMPLES</span></span>

### <span data-ttu-id="e375a-111">範例1</span><span class="sxs-lookup"><span data-stu-id="e375a-111">Example 1</span></span>
```
PS C:\>Set-AzEventHubGeoDRConfigurationFailOver -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Secondary" -Name "SampleDRConfigName"
```

<span data-ttu-id="e375a-112">針對別名 "SampleDRConfigName" 調用容錯移轉，重新配置並指向次要命名空間 "SampleNamespace_Secondary"</span><span class="sxs-lookup"><span data-stu-id="e375a-112">Invokes the Failover over alias "SampleDRConfigName", reconfigures and point to Secondary namespace "SampleNamespace_Secondary"</span></span>

## <span data-ttu-id="e375a-113">參數</span><span class="sxs-lookup"><span data-stu-id="e375a-113">PARAMETERS</span></span>

### <span data-ttu-id="e375a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e375a-114">-DefaultProfile</span></span>
<span data-ttu-id="e375a-115">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e375a-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e375a-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e375a-116">-InputObject</span></span>
<span data-ttu-id="e375a-117">Eventhub GeoDR Configuration 物件</span><span class="sxs-lookup"><span data-stu-id="e375a-117">Eventhub GeoDR Configuration Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventHub.Models.PSEventHubDRConfigurationAttributes
Parameter Sets: GeoDRConfigurationInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e375a-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="e375a-118">-Name</span></span>
<span data-ttu-id="e375a-119">DR 配置名稱</span><span class="sxs-lookup"><span data-stu-id="e375a-119">DR Configuration Name</span></span>

```yaml
Type: System.String
Parameter Sets: GeoDRParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e375a-120">-命名空間</span><span class="sxs-lookup"><span data-stu-id="e375a-120">-Namespace</span></span>
<span data-ttu-id="e375a-121">命名空間名稱-次要命名空間</span><span class="sxs-lookup"><span data-stu-id="e375a-121">Namespace Name - Secondary Namespace</span></span>

```yaml
Type: System.String
Parameter Sets: GeoDRParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e375a-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e375a-122">-PassThru</span></span>
<span data-ttu-id="e375a-123">傳回代表您正在使用之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="e375a-123">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="e375a-124">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="e375a-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="e375a-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e375a-125">-ResourceGroupName</span></span>
<span data-ttu-id="e375a-126">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="e375a-126">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: GeoDRParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e375a-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e375a-127">-ResourceId</span></span>
<span data-ttu-id="e375a-128">GeoDRConfiguration 資源識別碼</span><span class="sxs-lookup"><span data-stu-id="e375a-128">GeoDRConfiguration Resource Id</span></span>

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

### <span data-ttu-id="e375a-129">-確認</span><span class="sxs-lookup"><span data-stu-id="e375a-129">-Confirm</span></span>
<span data-ttu-id="e375a-130">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="e375a-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e375a-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e375a-131">-WhatIf</span></span>
<span data-ttu-id="e375a-132">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="e375a-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e375a-133">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e375a-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e375a-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e375a-134">CommonParameters</span></span>
<span data-ttu-id="e375a-135">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e375a-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e375a-136">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="e375a-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e375a-137">輸入</span><span class="sxs-lookup"><span data-stu-id="e375a-137">INPUTS</span></span>

### <span data-ttu-id="e375a-138">System.object</span><span class="sxs-lookup"><span data-stu-id="e375a-138">System.String</span></span>

### <span data-ttu-id="e375a-139">PSEventHubDRConfigurationAttributes 的 [.]</span><span class="sxs-lookup"><span data-stu-id="e375a-139">Microsoft.Azure.Commands.EventHub.Models.PSEventHubDRConfigurationAttributes</span></span>

## <span data-ttu-id="e375a-140">輸出</span><span class="sxs-lookup"><span data-stu-id="e375a-140">OUTPUTS</span></span>

### <span data-ttu-id="e375a-141">System.object</span><span class="sxs-lookup"><span data-stu-id="e375a-141">System.Boolean</span></span>

## <span data-ttu-id="e375a-142">筆記</span><span class="sxs-lookup"><span data-stu-id="e375a-142">NOTES</span></span>

## <span data-ttu-id="e375a-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="e375a-143">RELATED LINKS</span></span>