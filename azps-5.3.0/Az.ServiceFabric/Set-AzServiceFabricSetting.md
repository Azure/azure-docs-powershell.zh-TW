---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/set-azservicefabricsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Set-AzServiceFabricSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Set-AzServiceFabricSetting.md
ms.openlocfilehash: 871f3ba59fb84cea10200a7983fe7ee80b68918e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98439048"
---
# <span data-ttu-id="63569-101">Set-AzServiceFabricSetting</span><span class="sxs-lookup"><span data-stu-id="63569-101">Set-AzServiceFabricSetting</span></span>

## <span data-ttu-id="63569-102">摘要</span><span class="sxs-lookup"><span data-stu-id="63569-102">SYNOPSIS</span></span>
<span data-ttu-id="63569-103">在群集中新增或更新一或多個 Service Fabric 設定。</span><span class="sxs-lookup"><span data-stu-id="63569-103">Add or update one or multiple Service Fabric settings to the cluster.</span></span>

## <span data-ttu-id="63569-104">句法</span><span class="sxs-lookup"><span data-stu-id="63569-104">SYNTAX</span></span>

### <span data-ttu-id="63569-105">OneSetting</span><span class="sxs-lookup"><span data-stu-id="63569-105">OneSetting</span></span>
```
Set-AzServiceFabricSetting [-ResourceGroupName] <String> [-Name] <String> -Section <String> -Parameter <String>
 -Value <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="63569-106">BatchSettings</span><span class="sxs-lookup"><span data-stu-id="63569-106">BatchSettings</span></span>
```
Set-AzServiceFabricSetting [-ResourceGroupName] <String> [-Name] <String>
 -SettingsSectionDescription <PSSettingsSectionDescription[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="63569-107">說明</span><span class="sxs-lookup"><span data-stu-id="63569-107">DESCRIPTION</span></span>
<span data-ttu-id="63569-108">使用 [ **設定] AzServiceFabricSetting** 在群集中新增或更新 Service Fabric 設定。</span><span class="sxs-lookup"><span data-stu-id="63569-108">Use **Set-AzServiceFabricSetting** to add or update Service Fabric settings in a cluster.</span></span>

## <span data-ttu-id="63569-109">示例</span><span class="sxs-lookup"><span data-stu-id="63569-109">EXAMPLES</span></span>

### <span data-ttu-id="63569-110">範例1</span><span class="sxs-lookup"><span data-stu-id="63569-110">Example 1</span></span>
```
Set-AzServiceFabricSetting -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster'  -Section 'NamingService' -Parameter 'MaxFileOperationTimeout' -Value 5000
```

<span data-ttu-id="63569-111">這個命令會將 [MaxFileOperationTimeout] 設定為「NamingService」區段下的值 ' 5000」。</span><span class="sxs-lookup"><span data-stu-id="63569-111">This command will set 'MaxFileOperationTimeout' to value '5000' under the section 'NamingService'.</span></span>


### <span data-ttu-id="63569-112">範例2</span><span class="sxs-lookup"><span data-stu-id="63569-112">Example 2</span></span>
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

<span data-ttu-id="63569-113">這個命令會觸發升級以使用 SettingsSectionDescription 參數設定多個結構設定。</span><span class="sxs-lookup"><span data-stu-id="63569-113">This command will trigger an upgrade to set multiple fabric setting using SettingsSectionDescription parameter.</span></span>

## <span data-ttu-id="63569-114">參數</span><span class="sxs-lookup"><span data-stu-id="63569-114">PARAMETERS</span></span>

### <span data-ttu-id="63569-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="63569-115">-DefaultProfile</span></span>
<span data-ttu-id="63569-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="63569-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="63569-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="63569-117">-Name</span></span>
<span data-ttu-id="63569-118">指定群集的名稱</span><span class="sxs-lookup"><span data-stu-id="63569-118">Specify the name of the cluster</span></span>

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

### <span data-ttu-id="63569-119">-參數</span><span class="sxs-lookup"><span data-stu-id="63569-119">-Parameter</span></span>
<span data-ttu-id="63569-120">結構設定的參數名稱</span><span class="sxs-lookup"><span data-stu-id="63569-120">Parameter name of the fabric setting</span></span>

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

### <span data-ttu-id="63569-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="63569-121">-ResourceGroupName</span></span>
<span data-ttu-id="63569-122">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="63569-122">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="63569-123">區段</span><span class="sxs-lookup"><span data-stu-id="63569-123">-Section</span></span>
<span data-ttu-id="63569-124">結構設定的章節名稱</span><span class="sxs-lookup"><span data-stu-id="63569-124">Section name of the fabric setting</span></span>

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

### <span data-ttu-id="63569-125">-SettingsSectionDescription</span><span class="sxs-lookup"><span data-stu-id="63569-125">-SettingsSectionDescription</span></span>
<span data-ttu-id="63569-126">結構設定陣列</span><span class="sxs-lookup"><span data-stu-id="63569-126">An array of fabric settings</span></span>

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

### <span data-ttu-id="63569-127">-值</span><span class="sxs-lookup"><span data-stu-id="63569-127">-Value</span></span>
<span data-ttu-id="63569-128">結構設定的參數值</span><span class="sxs-lookup"><span data-stu-id="63569-128">Parameter value of the fabric setting</span></span>

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

### <span data-ttu-id="63569-129">-確認</span><span class="sxs-lookup"><span data-stu-id="63569-129">-Confirm</span></span>
<span data-ttu-id="63569-130">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="63569-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="63569-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="63569-131">-WhatIf</span></span>
<span data-ttu-id="63569-132">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="63569-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="63569-133">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="63569-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="63569-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63569-134">CommonParameters</span></span>
<span data-ttu-id="63569-135">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="63569-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63569-136">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="63569-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63569-137">輸入</span><span class="sxs-lookup"><span data-stu-id="63569-137">INPUTS</span></span>

### <span data-ttu-id="63569-138">System.object</span><span class="sxs-lookup"><span data-stu-id="63569-138">System.String</span></span>

### <span data-ttu-id="63569-139">PSSettingsSectionDescription [] 的 ServiceFabric []</span><span class="sxs-lookup"><span data-stu-id="63569-139">Microsoft.Azure.Commands.ServiceFabric.Models.PSSettingsSectionDescription[]</span></span>

## <span data-ttu-id="63569-140">輸出</span><span class="sxs-lookup"><span data-stu-id="63569-140">OUTPUTS</span></span>

### <span data-ttu-id="63569-141">PSCluster 中的 ServiceFabric。</span><span class="sxs-lookup"><span data-stu-id="63569-141">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="63569-142">筆記</span><span class="sxs-lookup"><span data-stu-id="63569-142">NOTES</span></span>

## <span data-ttu-id="63569-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="63569-143">RELATED LINKS</span></span>
