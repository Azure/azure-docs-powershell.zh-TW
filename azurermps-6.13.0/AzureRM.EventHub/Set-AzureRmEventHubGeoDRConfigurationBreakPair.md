---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/set-azurermeventhubgeodrconfigurationbreakpair
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Set-AzureRmEventHubGeoDRConfigurationBreakPair.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Set-AzureRmEventHubGeoDRConfigurationBreakPair.md
ms.openlocfilehash: 3ee0e251f4dd92b087343edc03e829e8032ee5c8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93449174"
---
# <span data-ttu-id="21390-101">Set-AzureRmEventHubGeoDRConfigurationBreakPair</span><span class="sxs-lookup"><span data-stu-id="21390-101">Set-AzureRmEventHubGeoDRConfigurationBreakPair</span></span>

## <span data-ttu-id="21390-102">摘要</span><span class="sxs-lookup"><span data-stu-id="21390-102">SYNOPSIS</span></span>
<span data-ttu-id="21390-103">這個作業會停用災害復原，並停止將主要的變更複製到次要命名空間</span><span class="sxs-lookup"><span data-stu-id="21390-103">This operation disables the Disaster Recovery and stops replicating changes from primary to secondary namespaces</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="21390-104">句法</span><span class="sxs-lookup"><span data-stu-id="21390-104">SYNTAX</span></span>

### <span data-ttu-id="21390-105">GeoDRParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="21390-105">GeoDRParameterSet (Default)</span></span>
```
Set-AzureRmEventHubGeoDRConfigurationBreakPair [-ResourceGroupName] <String> [-Namespace] <String>
 [-Name] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="21390-106">GeoDRConfigurationInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="21390-106">GeoDRConfigurationInputObjectSet</span></span>
```
Set-AzureRmEventHubGeoDRConfigurationBreakPair [-InputObject] <PSEventHubDRConfigurationAttributes> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="21390-107">GeoDRConfigResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="21390-107">GeoDRConfigResourceIdParameterSet</span></span>
```
Set-AzureRmEventHubGeoDRConfigurationBreakPair [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="21390-108">說明</span><span class="sxs-lookup"><span data-stu-id="21390-108">DESCRIPTION</span></span>
<span data-ttu-id="21390-109">**AzureRmEventHubGeoDRConfigurationBreakPair** Cmdlet 會停用災害復原，並停止將主要的變更複製到次要命名空間</span><span class="sxs-lookup"><span data-stu-id="21390-109">The **Set-AzureRmEventHubGeoDRConfigurationBreakPair** cmdlet disables the Disaster Recovery and stops replicating changes from primary to secondary namespaces</span></span>

## <span data-ttu-id="21390-110">示例</span><span class="sxs-lookup"><span data-stu-id="21390-110">EXAMPLES</span></span>

### <span data-ttu-id="21390-111">範例</span><span class="sxs-lookup"><span data-stu-id="21390-111">Example</span></span>
```
PS C:\> Set-AzureRmEventHubGeoDRConfigurationBreakPair -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Primary" -Name "SampleDRCongifName"
```

<span data-ttu-id="21390-112">這個作業會停用災害復原，並停止將主要的變更複製到次要命名空間</span><span class="sxs-lookup"><span data-stu-id="21390-112">This operation disables the Disaster Recovery and stops replicating changes from primary to secondary namespaces</span></span>

## <span data-ttu-id="21390-113">參數</span><span class="sxs-lookup"><span data-stu-id="21390-113">PARAMETERS</span></span>

### <span data-ttu-id="21390-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="21390-114">-DefaultProfile</span></span>
<span data-ttu-id="21390-115">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="21390-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="21390-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="21390-116">-InputObject</span></span>
<span data-ttu-id="21390-117">Eventhub GeoDR Configuration 物件</span><span class="sxs-lookup"><span data-stu-id="21390-117">Eventhub GeoDR Configuration Object</span></span>

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

### <span data-ttu-id="21390-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="21390-118">-Name</span></span>
<span data-ttu-id="21390-119">DR 配置名稱</span><span class="sxs-lookup"><span data-stu-id="21390-119">DR Configuration Name</span></span>

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

### <span data-ttu-id="21390-120">-命名空間</span><span class="sxs-lookup"><span data-stu-id="21390-120">-Namespace</span></span>
<span data-ttu-id="21390-121">命名空間名稱-主要命名空間</span><span class="sxs-lookup"><span data-stu-id="21390-121">Namespace Name - Primary Namespace</span></span>

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

### <span data-ttu-id="21390-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="21390-122">-PassThru</span></span>
<span data-ttu-id="21390-123">傳回代表您正在使用之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="21390-123">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="21390-124">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="21390-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="21390-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="21390-125">-ResourceGroupName</span></span>
<span data-ttu-id="21390-126">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="21390-126">Resource Group Name</span></span>

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

### <span data-ttu-id="21390-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="21390-127">-ResourceId</span></span>
<span data-ttu-id="21390-128">GeoDRConfiguration 資源識別碼</span><span class="sxs-lookup"><span data-stu-id="21390-128">GeoDRConfiguration Resource Id</span></span>

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

### <span data-ttu-id="21390-129">-確認</span><span class="sxs-lookup"><span data-stu-id="21390-129">-Confirm</span></span>
<span data-ttu-id="21390-130">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="21390-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="21390-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="21390-131">-WhatIf</span></span>
<span data-ttu-id="21390-132">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="21390-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="21390-133">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="21390-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="21390-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21390-134">CommonParameters</span></span>
<span data-ttu-id="21390-135">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="21390-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21390-136">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="21390-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21390-137">輸入</span><span class="sxs-lookup"><span data-stu-id="21390-137">INPUTS</span></span>

### <span data-ttu-id="21390-138">System.object</span><span class="sxs-lookup"><span data-stu-id="21390-138">System.String</span></span>

### <span data-ttu-id="21390-139">PSEventHubDRConfigurationAttributes 的 [.]</span><span class="sxs-lookup"><span data-stu-id="21390-139">Microsoft.Azure.Commands.EventHub.Models.PSEventHubDRConfigurationAttributes</span></span>
<span data-ttu-id="21390-140">參數： InputObject (ByValue) </span><span class="sxs-lookup"><span data-stu-id="21390-140">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="21390-141">輸出</span><span class="sxs-lookup"><span data-stu-id="21390-141">OUTPUTS</span></span>

### <span data-ttu-id="21390-142">System.object</span><span class="sxs-lookup"><span data-stu-id="21390-142">System.Boolean</span></span>

## <span data-ttu-id="21390-143">筆記</span><span class="sxs-lookup"><span data-stu-id="21390-143">NOTES</span></span>

## <span data-ttu-id="21390-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="21390-144">RELATED LINKS</span></span>
