---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/set-azurermeventhubgeodrconfigurationfailover
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Set-AzureRmEventHubGeoDRConfigurationFailOver.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Set-AzureRmEventHubGeoDRConfigurationFailOver.md
ms.openlocfilehash: 0da9ecf9fabaa1cbb21a5fe8f82bb172b84850e6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93623978"
---
# <span data-ttu-id="ef713-101">Set-AzureRmEventHubGeoDRConfigurationFailOver</span><span class="sxs-lookup"><span data-stu-id="ef713-101">Set-AzureRmEventHubGeoDRConfigurationFailOver</span></span>

## <span data-ttu-id="ef713-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ef713-102">SYNOPSIS</span></span>
<span data-ttu-id="ef713-103">調用 GEO DR 容錯移轉，並重新設定別名以指向次要命名空間</span><span class="sxs-lookup"><span data-stu-id="ef713-103">Invokes GEO DR failover and reconfigure the alias to point to the secondary namespace</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ef713-104">句法</span><span class="sxs-lookup"><span data-stu-id="ef713-104">SYNTAX</span></span>

### <span data-ttu-id="ef713-105">GeoDRParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="ef713-105">GeoDRParameterSet (Default)</span></span>
```
Set-AzureRmEventHubGeoDRConfigurationFailOver [-ResourceGroupName] <String> [-Namespace] <String>
 [-Name] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ef713-106">GeoDRConfigurationInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="ef713-106">GeoDRConfigurationInputObjectSet</span></span>
```
Set-AzureRmEventHubGeoDRConfigurationFailOver [-InputObject] <PSEventHubDRConfigurationAttributes> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ef713-107">GeoDRConfigResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ef713-107">GeoDRConfigResourceIdParameterSet</span></span>
```
Set-AzureRmEventHubGeoDRConfigurationFailOver [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ef713-108">說明</span><span class="sxs-lookup"><span data-stu-id="ef713-108">DESCRIPTION</span></span>
<span data-ttu-id="ef713-109">**AzureRmEventHubGeoDRConfigurationFailOver** CMDLET ENVOKES GEO DR 容錯移轉，並將別名重新設定為指向次要命名空間</span><span class="sxs-lookup"><span data-stu-id="ef713-109">The **Set-AzureRmEventHubGeoDRConfigurationFailOver** cmdlet envokes GEO DR failover and reconfigure the alias to point to the secondary namespace</span></span>

## <span data-ttu-id="ef713-110">示例</span><span class="sxs-lookup"><span data-stu-id="ef713-110">EXAMPLES</span></span>

### <span data-ttu-id="ef713-111">範例1</span><span class="sxs-lookup"><span data-stu-id="ef713-111">Example 1</span></span>
```
PS C:\>Set-AzureRmEventHubGeoDRConfigurationFailOver -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Secondary" -Name "SampleDRCongifName"
```

<span data-ttu-id="ef713-112">針對別名 "SampleDRCongifName" 調用容錯移轉，重新配置並指向次要命名空間 "SampleNamespace_Secondary"</span><span class="sxs-lookup"><span data-stu-id="ef713-112">Invokes the Failover over alias "SampleDRCongifName", reconfigures and point to Secondary namespace "SampleNamespace_Secondary"</span></span>

## <span data-ttu-id="ef713-113">參數</span><span class="sxs-lookup"><span data-stu-id="ef713-113">PARAMETERS</span></span>

### <span data-ttu-id="ef713-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef713-114">-DefaultProfile</span></span>
<span data-ttu-id="ef713-115">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="ef713-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef713-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ef713-116">-InputObject</span></span>
<span data-ttu-id="ef713-117">Eventhub GeoDR Configuration 物件</span><span class="sxs-lookup"><span data-stu-id="ef713-117">Eventhub GeoDR Configuration Object</span></span>

```yaml
Type: PSEventHubDRConfigurationAttributes
Parameter Sets: GeoDRConfigurationInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ef713-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="ef713-118">-Name</span></span>
<span data-ttu-id="ef713-119">DR 配置名稱</span><span class="sxs-lookup"><span data-stu-id="ef713-119">DR Configuration Name</span></span>

```yaml
Type: String
Parameter Sets: GeoDRParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ef713-120">-命名空間</span><span class="sxs-lookup"><span data-stu-id="ef713-120">-Namespace</span></span>
<span data-ttu-id="ef713-121">命名空間名稱-次要命名空間</span><span class="sxs-lookup"><span data-stu-id="ef713-121">Namespace Name - Secondary Namespace</span></span>

```yaml
Type: String
Parameter Sets: GeoDRParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ef713-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ef713-122">-PassThru</span></span>
<span data-ttu-id="ef713-123">傳回代表您正在使用之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="ef713-123">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="ef713-124">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="ef713-124">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef713-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ef713-125">-ResourceGroupName</span></span>
<span data-ttu-id="ef713-126">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="ef713-126">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: GeoDRParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ef713-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ef713-127">-ResourceId</span></span>
<span data-ttu-id="ef713-128">GeoDRConfiguration 資源識別碼</span><span class="sxs-lookup"><span data-stu-id="ef713-128">GeoDRConfiguration Resource Id</span></span>

```yaml
Type: String
Parameter Sets: GeoDRConfigResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ef713-129">-確認</span><span class="sxs-lookup"><span data-stu-id="ef713-129">-Confirm</span></span>
<span data-ttu-id="ef713-130">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="ef713-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef713-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ef713-131">-WhatIf</span></span>
<span data-ttu-id="ef713-132">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ef713-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ef713-133">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ef713-133">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef713-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef713-134">CommonParameters</span></span>
<span data-ttu-id="ef713-135">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ef713-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="ef713-136">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="ef713-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef713-137">輸入</span><span class="sxs-lookup"><span data-stu-id="ef713-137">INPUTS</span></span>

### <span data-ttu-id="ef713-138">System.object</span><span class="sxs-lookup"><span data-stu-id="ef713-138">System.String</span></span>
<span data-ttu-id="ef713-139">PSEventHubDRConfigurationAttributes 的 [.]</span><span class="sxs-lookup"><span data-stu-id="ef713-139">Microsoft.Azure.Commands.EventHub.Models.PSEventHubDRConfigurationAttributes</span></span>


## <span data-ttu-id="ef713-140">輸出</span><span class="sxs-lookup"><span data-stu-id="ef713-140">OUTPUTS</span></span>

### <span data-ttu-id="ef713-141">System.object</span><span class="sxs-lookup"><span data-stu-id="ef713-141">System.Boolean</span></span>


## <span data-ttu-id="ef713-142">筆記</span><span class="sxs-lookup"><span data-stu-id="ef713-142">NOTES</span></span>

## <span data-ttu-id="ef713-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="ef713-143">RELATED LINKS</span></span>
