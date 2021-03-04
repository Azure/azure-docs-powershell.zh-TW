---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/powershell/module/az.eventhub/set-azeventhubgeodrconfigurationfailover
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubGeoDRConfigurationFailOver.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubGeoDRConfigurationFailOver.md
ms.openlocfilehash: d68fe2005f827d55b57ecedb7e21fd11b0cc9978
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101910494"
---
# <span data-ttu-id="dbaae-101">Set-AzEventHubGeoDRConfigurationFailOver</span><span class="sxs-lookup"><span data-stu-id="dbaae-101">Set-AzEventHubGeoDRConfigurationFailOver</span></span>

## <span data-ttu-id="dbaae-102">簡介</span><span class="sxs-lookup"><span data-stu-id="dbaae-102">SYNOPSIS</span></span>
<span data-ttu-id="dbaae-103">會調用 GEO DR 容錯移轉，並重新指定別名以指向次要命名空間</span><span class="sxs-lookup"><span data-stu-id="dbaae-103">Invokes GEO DR failover and reconfigure the alias to point to the secondary namespace</span></span>

## <span data-ttu-id="dbaae-104">語法</span><span class="sxs-lookup"><span data-stu-id="dbaae-104">SYNTAX</span></span>

### <span data-ttu-id="dbaae-105">GeoDRParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="dbaae-105">GeoDRParameterSet (Default)</span></span>
```
Set-AzEventHubGeoDRConfigurationFailOver [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dbaae-106">GeoDRConfigurationInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="dbaae-106">GeoDRConfigurationInputObjectSet</span></span>
```
Set-AzEventHubGeoDRConfigurationFailOver [-InputObject] <PSEventHubDRConfigurationAttributes> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dbaae-107">GeoDRConfigResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="dbaae-107">GeoDRConfigResourceIdParameterSet</span></span>
```
Set-AzEventHubGeoDRConfigurationFailOver [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dbaae-108">描述</span><span class="sxs-lookup"><span data-stu-id="dbaae-108">DESCRIPTION</span></span>
<span data-ttu-id="dbaae-109">**Set-AzEventHubGeoDRConfigurationFailOver** Cmdlet 會調用 GEO DR 容錯移轉，並重新設定別名以指向次要命名空間</span><span class="sxs-lookup"><span data-stu-id="dbaae-109">The **Set-AzEventHubGeoDRConfigurationFailOver** cmdlet invokes GEO DR failover and reconfigure the alias to point to the secondary namespace</span></span>

## <span data-ttu-id="dbaae-110">例子</span><span class="sxs-lookup"><span data-stu-id="dbaae-110">EXAMPLES</span></span>

### <span data-ttu-id="dbaae-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="dbaae-111">Example 1</span></span>
```
PS C:\>Set-AzEventHubGeoDRConfigurationFailOver -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Secondary" -Name "SampleDRConfigName"
```

<span data-ttu-id="dbaae-112">在別名 "SampleDRConfigName" 上調用容錯移轉，重新指定並指向次要命名空間 "SampleNamespace_Secondary"</span><span class="sxs-lookup"><span data-stu-id="dbaae-112">Invokes the Failover over alias "SampleDRConfigName", reconfigures and point to Secondary namespace "SampleNamespace_Secondary"</span></span>

## <span data-ttu-id="dbaae-113">參數</span><span class="sxs-lookup"><span data-stu-id="dbaae-113">PARAMETERS</span></span>

### <span data-ttu-id="dbaae-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dbaae-114">-DefaultProfile</span></span>
<span data-ttu-id="dbaae-115">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="dbaae-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dbaae-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dbaae-116">-InputObject</span></span>
<span data-ttu-id="dbaae-117">Eventhub GeoDR Configuration Object</span><span class="sxs-lookup"><span data-stu-id="dbaae-117">Eventhub GeoDR Configuration Object</span></span>

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

### <span data-ttu-id="dbaae-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="dbaae-118">-Name</span></span>
<span data-ttu-id="dbaae-119">DR 組組名稱</span><span class="sxs-lookup"><span data-stu-id="dbaae-119">DR Configuration Name</span></span>

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

### <span data-ttu-id="dbaae-120">-命名空間</span><span class="sxs-lookup"><span data-stu-id="dbaae-120">-Namespace</span></span>
<span data-ttu-id="dbaae-121">命名空間名稱 - 次要命名空間</span><span class="sxs-lookup"><span data-stu-id="dbaae-121">Namespace Name - Secondary Namespace</span></span>

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

### <span data-ttu-id="dbaae-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="dbaae-122">-PassThru</span></span>
<span data-ttu-id="dbaae-123">會返回代表您處理之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="dbaae-123">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="dbaae-124">根據預設，此 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="dbaae-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="dbaae-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dbaae-125">-ResourceGroupName</span></span>
<span data-ttu-id="dbaae-126">資源組名</span><span class="sxs-lookup"><span data-stu-id="dbaae-126">Resource Group Name</span></span>

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

### <span data-ttu-id="dbaae-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="dbaae-127">-ResourceId</span></span>
<span data-ttu-id="dbaae-128">GeoDRConfiguration 資源識別碼</span><span class="sxs-lookup"><span data-stu-id="dbaae-128">GeoDRConfiguration Resource Id</span></span>

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

### <span data-ttu-id="dbaae-129">-確認</span><span class="sxs-lookup"><span data-stu-id="dbaae-129">-Confirm</span></span>
<span data-ttu-id="dbaae-130">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="dbaae-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dbaae-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dbaae-131">-WhatIf</span></span>
<span data-ttu-id="dbaae-132">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="dbaae-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dbaae-133">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="dbaae-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dbaae-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dbaae-134">CommonParameters</span></span>
<span data-ttu-id="dbaae-135">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="dbaae-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dbaae-136">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="dbaae-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dbaae-137">輸入</span><span class="sxs-lookup"><span data-stu-id="dbaae-137">INPUTS</span></span>

### <span data-ttu-id="dbaae-138">System.String</span><span class="sxs-lookup"><span data-stu-id="dbaae-138">System.String</span></span>

### <span data-ttu-id="dbaae-139">Microsoft.Azure.Commands.EventHub.models.PSEventHubDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="dbaae-139">Microsoft.Azure.Commands.EventHub.Models.PSEventHubDRConfigurationAttributes</span></span>

## <span data-ttu-id="dbaae-140">輸出</span><span class="sxs-lookup"><span data-stu-id="dbaae-140">OUTPUTS</span></span>

### <span data-ttu-id="dbaae-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="dbaae-141">System.Boolean</span></span>

## <span data-ttu-id="dbaae-142">筆記</span><span class="sxs-lookup"><span data-stu-id="dbaae-142">NOTES</span></span>

## <span data-ttu-id="dbaae-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="dbaae-143">RELATED LINKS</span></span>
