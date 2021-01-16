---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/set-azservicefabricsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Set-AzServiceFabricSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Set-AzServiceFabricSetting.md
ms.openlocfilehash: 871f3ba59fb84cea10200a7983fe7ee80b68918e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98282147"
---
# <span data-ttu-id="6c4aa-101">Set-AzServiceFabricSetting</span><span class="sxs-lookup"><span data-stu-id="6c4aa-101">Set-AzServiceFabricSetting</span></span>

## <span data-ttu-id="6c4aa-102">摘要</span><span class="sxs-lookup"><span data-stu-id="6c4aa-102">SYNOPSIS</span></span>
<span data-ttu-id="6c4aa-103">在群集中新增或更新一或多個 Service Fabric 設定。</span><span class="sxs-lookup"><span data-stu-id="6c4aa-103">Add or update one or multiple Service Fabric settings to the cluster.</span></span>

## <span data-ttu-id="6c4aa-104">句法</span><span class="sxs-lookup"><span data-stu-id="6c4aa-104">SYNTAX</span></span>

### <span data-ttu-id="6c4aa-105">OneSetting</span><span class="sxs-lookup"><span data-stu-id="6c4aa-105">OneSetting</span></span>
```
Set-AzServiceFabricSetting [-ResourceGroupName] <String> [-Name] <String> -Section <String> -Parameter <String>
 -Value <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6c4aa-106">BatchSettings</span><span class="sxs-lookup"><span data-stu-id="6c4aa-106">BatchSettings</span></span>
```
Set-AzServiceFabricSetting [-ResourceGroupName] <String> [-Name] <String>
 -SettingsSectionDescription <PSSettingsSectionDescription[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6c4aa-107">說明</span><span class="sxs-lookup"><span data-stu-id="6c4aa-107">DESCRIPTION</span></span>
<span data-ttu-id="6c4aa-108">使用 [ **設定] AzServiceFabricSetting** 在群集中新增或更新 Service Fabric 設定。</span><span class="sxs-lookup"><span data-stu-id="6c4aa-108">Use **Set-AzServiceFabricSetting** to add or update Service Fabric settings in a cluster.</span></span>

## <span data-ttu-id="6c4aa-109">示例</span><span class="sxs-lookup"><span data-stu-id="6c4aa-109">EXAMPLES</span></span>

### <span data-ttu-id="6c4aa-110">範例1</span><span class="sxs-lookup"><span data-stu-id="6c4aa-110">Example 1</span></span>
```
Set-AzServiceFabricSetting -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster'  -Section 'NamingService' -Parameter 'MaxFileOperationTimeout' -Value 5000
```

<span data-ttu-id="6c4aa-111">這個命令會將 [MaxFileOperationTimeout] 設定為「NamingService」區段下的值 ' 5000」。</span><span class="sxs-lookup"><span data-stu-id="6c4aa-111">This command will set 'MaxFileOperationTimeout' to value '5000' under the section 'NamingService'.</span></span>


### <span data-ttu-id="6c4aa-112">範例2</span><span class="sxs-lookup"><span data-stu-id="6c4aa-112">Example 2</span></span>
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

<span data-ttu-id="6c4aa-113">這個命令會觸發升級以使用 SettingsSectionDescription 參數設定多個結構設定。</span><span class="sxs-lookup"><span data-stu-id="6c4aa-113">This command will trigger an upgrade to set multiple fabric setting using SettingsSectionDescription parameter.</span></span>

## <span data-ttu-id="6c4aa-114">參數</span><span class="sxs-lookup"><span data-stu-id="6c4aa-114">PARAMETERS</span></span>

### <span data-ttu-id="6c4aa-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6c4aa-115">-DefaultProfile</span></span>
<span data-ttu-id="6c4aa-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="6c4aa-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6c4aa-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="6c4aa-117">-Name</span></span>
<span data-ttu-id="6c4aa-118">指定群集的名稱</span><span class="sxs-lookup"><span data-stu-id="6c4aa-118">Specify the name of the cluster</span></span>

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

### <span data-ttu-id="6c4aa-119">-參數</span><span class="sxs-lookup"><span data-stu-id="6c4aa-119">-Parameter</span></span>
<span data-ttu-id="6c4aa-120">結構設定的參數名稱</span><span class="sxs-lookup"><span data-stu-id="6c4aa-120">Parameter name of the fabric setting</span></span>

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

### <span data-ttu-id="6c4aa-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6c4aa-121">-ResourceGroupName</span></span>
<span data-ttu-id="6c4aa-122">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="6c4aa-122">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="6c4aa-123">區段</span><span class="sxs-lookup"><span data-stu-id="6c4aa-123">-Section</span></span>
<span data-ttu-id="6c4aa-124">結構設定的章節名稱</span><span class="sxs-lookup"><span data-stu-id="6c4aa-124">Section name of the fabric setting</span></span>

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

### <span data-ttu-id="6c4aa-125">-SettingsSectionDescription</span><span class="sxs-lookup"><span data-stu-id="6c4aa-125">-SettingsSectionDescription</span></span>
<span data-ttu-id="6c4aa-126">結構設定陣列</span><span class="sxs-lookup"><span data-stu-id="6c4aa-126">An array of fabric settings</span></span>

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

### <span data-ttu-id="6c4aa-127">-值</span><span class="sxs-lookup"><span data-stu-id="6c4aa-127">-Value</span></span>
<span data-ttu-id="6c4aa-128">結構設定的參數值</span><span class="sxs-lookup"><span data-stu-id="6c4aa-128">Parameter value of the fabric setting</span></span>

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

### <span data-ttu-id="6c4aa-129">-確認</span><span class="sxs-lookup"><span data-stu-id="6c4aa-129">-Confirm</span></span>
<span data-ttu-id="6c4aa-130">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="6c4aa-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6c4aa-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6c4aa-131">-WhatIf</span></span>
<span data-ttu-id="6c4aa-132">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="6c4aa-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6c4aa-133">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6c4aa-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6c4aa-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c4aa-134">CommonParameters</span></span>
<span data-ttu-id="6c4aa-135">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="6c4aa-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6c4aa-136">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="6c4aa-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c4aa-137">輸入</span><span class="sxs-lookup"><span data-stu-id="6c4aa-137">INPUTS</span></span>

### <span data-ttu-id="6c4aa-138">System.object</span><span class="sxs-lookup"><span data-stu-id="6c4aa-138">System.String</span></span>

### <span data-ttu-id="6c4aa-139">PSSettingsSectionDescription [] 的 ServiceFabric []</span><span class="sxs-lookup"><span data-stu-id="6c4aa-139">Microsoft.Azure.Commands.ServiceFabric.Models.PSSettingsSectionDescription[]</span></span>

## <span data-ttu-id="6c4aa-140">輸出</span><span class="sxs-lookup"><span data-stu-id="6c4aa-140">OUTPUTS</span></span>

### <span data-ttu-id="6c4aa-141">PSCluster 中的 ServiceFabric。</span><span class="sxs-lookup"><span data-stu-id="6c4aa-141">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="6c4aa-142">筆記</span><span class="sxs-lookup"><span data-stu-id="6c4aa-142">NOTES</span></span>

## <span data-ttu-id="6c4aa-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="6c4aa-143">RELATED LINKS</span></span>
