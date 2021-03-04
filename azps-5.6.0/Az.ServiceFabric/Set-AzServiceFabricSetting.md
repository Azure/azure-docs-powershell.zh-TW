---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/powershell/module/az.servicefabric/set-azservicefabricsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Set-AzServiceFabricSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Set-AzServiceFabricSetting.md
ms.openlocfilehash: f98a5efeece2eb1e78479c3f76de62db495c6e43
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101908005"
---
# <span data-ttu-id="56dfc-101">Set-AzServiceFabricSetting</span><span class="sxs-lookup"><span data-stu-id="56dfc-101">Set-AzServiceFabricSetting</span></span>

## <span data-ttu-id="56dfc-102">簡介</span><span class="sxs-lookup"><span data-stu-id="56dfc-102">SYNOPSIS</span></span>
<span data-ttu-id="56dfc-103">新增或更新一或多個服務佈設定至該組。</span><span class="sxs-lookup"><span data-stu-id="56dfc-103">Add or update one or multiple Service Fabric settings to the cluster.</span></span>

## <span data-ttu-id="56dfc-104">語法</span><span class="sxs-lookup"><span data-stu-id="56dfc-104">SYNTAX</span></span>

### <span data-ttu-id="56dfc-105">OneSetting</span><span class="sxs-lookup"><span data-stu-id="56dfc-105">OneSetting</span></span>
```
Set-AzServiceFabricSetting [-ResourceGroupName] <String> [-Name] <String> -Section <String> -Parameter <String>
 -Value <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="56dfc-106">BatchSettings</span><span class="sxs-lookup"><span data-stu-id="56dfc-106">BatchSettings</span></span>
```
Set-AzServiceFabricSetting [-ResourceGroupName] <String> [-Name] <String>
 -SettingsSectionDescription <PSSettingsSectionDescription[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="56dfc-107">描述</span><span class="sxs-lookup"><span data-stu-id="56dfc-107">DESCRIPTION</span></span>
<span data-ttu-id="56dfc-108">使用 **Set-AzServiceFabricSetting** 新增或更新組集中的服務結構設定。</span><span class="sxs-lookup"><span data-stu-id="56dfc-108">Use **Set-AzServiceFabricSetting** to add or update Service Fabric settings in a cluster.</span></span>

## <span data-ttu-id="56dfc-109">例子</span><span class="sxs-lookup"><span data-stu-id="56dfc-109">EXAMPLES</span></span>

### <span data-ttu-id="56dfc-110">範例 1</span><span class="sxs-lookup"><span data-stu-id="56dfc-110">Example 1</span></span>
```
Set-AzServiceFabricSetting -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster'  -Section 'NamingService' -Parameter 'MaxFileOperationTimeout' -Value 5000
```

<span data-ttu-id="56dfc-111">此命令將設定 "MaxFileOperationTimeout" 值 '5000' 在 'NamingService' 區段下。</span><span class="sxs-lookup"><span data-stu-id="56dfc-111">This command will set 'MaxFileOperationTimeout' to value '5000' under the section 'NamingService'.</span></span>


### <span data-ttu-id="56dfc-112">範例 2</span><span class="sxs-lookup"><span data-stu-id="56dfc-112">Example 2</span></span>
```
$fabricSettings = @(
    @{ 
        "name" = "NamingService";
        "parameters" =  [System.Collections.Generic.List[Microsoft.Azure.Commands.ServiceFabric.Models.PSSettingsParameterDescription]]@(
            @{ "Name" = "MaxFileOperationTimeout"; "Value" = "5000"  };
            @{ "Name" = "MaxOperationTimeout"; "Value" = "1200"  })
    },
    @{ 
        "name" = "Hosting";
        "parameters" =  [System.Collections.Generic.List[Microsoft.Azure.Commands.ServiceFabric.Models.PSSettingsParameterDescription]]@(
            @{ "Name" = "ActivationMaxFailureCount"; "Value" = "11"  })
    })

Set-AzServiceFabricSetting -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -SettingsSectionDescription $fabricSettings -Verbose
```

<span data-ttu-id="56dfc-113">此命令會觸發升級，以使用 SettingsSectionDescription 參數設定多個布料設定。</span><span class="sxs-lookup"><span data-stu-id="56dfc-113">This command will trigger an upgrade to set multiple fabric setting using SettingsSectionDescription parameter.</span></span>

## <span data-ttu-id="56dfc-114">參數</span><span class="sxs-lookup"><span data-stu-id="56dfc-114">PARAMETERS</span></span>

### <span data-ttu-id="56dfc-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56dfc-115">-DefaultProfile</span></span>
<span data-ttu-id="56dfc-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="56dfc-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="56dfc-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="56dfc-117">-Name</span></span>
<span data-ttu-id="56dfc-118">指定組名</span><span class="sxs-lookup"><span data-stu-id="56dfc-118">Specify the name of the cluster</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ClusterName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="56dfc-119">-Parameter</span><span class="sxs-lookup"><span data-stu-id="56dfc-119">-Parameter</span></span>
<span data-ttu-id="56dfc-120">布料設定的參數名稱</span><span class="sxs-lookup"><span data-stu-id="56dfc-120">Parameter name of the fabric setting</span></span>

```yaml
Type: System.String
Parameter Sets: OneSetting
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="56dfc-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="56dfc-121">-ResourceGroupName</span></span>
<span data-ttu-id="56dfc-122">指定資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="56dfc-122">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="56dfc-123">-區段</span><span class="sxs-lookup"><span data-stu-id="56dfc-123">-Section</span></span>
<span data-ttu-id="56dfc-124">布料設定區段名稱</span><span class="sxs-lookup"><span data-stu-id="56dfc-124">Section name of the fabric setting</span></span>

```yaml
Type: System.String
Parameter Sets: OneSetting
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="56dfc-125">-SettingsSectionDescription</span><span class="sxs-lookup"><span data-stu-id="56dfc-125">-SettingsSectionDescription</span></span>
<span data-ttu-id="56dfc-126">布料設定陣列</span><span class="sxs-lookup"><span data-stu-id="56dfc-126">An array of fabric settings</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.PSSettingsSectionDescription[]
Parameter Sets: BatchSettings
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="56dfc-127">-值</span><span class="sxs-lookup"><span data-stu-id="56dfc-127">-Value</span></span>
<span data-ttu-id="56dfc-128">布料設定的參數值</span><span class="sxs-lookup"><span data-stu-id="56dfc-128">Parameter value of the fabric setting</span></span>

```yaml
Type: System.String
Parameter Sets: OneSetting
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="56dfc-129">-確認</span><span class="sxs-lookup"><span data-stu-id="56dfc-129">-Confirm</span></span>
<span data-ttu-id="56dfc-130">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="56dfc-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="56dfc-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="56dfc-131">-WhatIf</span></span>
<span data-ttu-id="56dfc-132">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="56dfc-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="56dfc-133">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="56dfc-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="56dfc-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56dfc-134">CommonParameters</span></span>
<span data-ttu-id="56dfc-135">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="56dfc-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56dfc-136">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="56dfc-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56dfc-137">輸入</span><span class="sxs-lookup"><span data-stu-id="56dfc-137">INPUTS</span></span>

### <span data-ttu-id="56dfc-138">System.String</span><span class="sxs-lookup"><span data-stu-id="56dfc-138">System.String</span></span>

### <span data-ttu-id="56dfc-139">Microsoft.Azure.Commands.ServiceFabric.Models.PSSettingsSectionDescription[]</span><span class="sxs-lookup"><span data-stu-id="56dfc-139">Microsoft.Azure.Commands.ServiceFabric.Models.PSSettingsSectionDescription[]</span></span>

## <span data-ttu-id="56dfc-140">輸出</span><span class="sxs-lookup"><span data-stu-id="56dfc-140">OUTPUTS</span></span>

### <span data-ttu-id="56dfc-141">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span><span class="sxs-lookup"><span data-stu-id="56dfc-141">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="56dfc-142">筆記</span><span class="sxs-lookup"><span data-stu-id="56dfc-142">NOTES</span></span>

## <span data-ttu-id="56dfc-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="56dfc-143">RELATED LINKS</span></span>
