---
external help file: Microsoft.Azure.Commands.ServiceFabric.dll-Help.xml
Module Name: AzureRM.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicefabric/set-azurermservicefabricsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Set-AzureRmServiceFabricSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Set-AzureRmServiceFabricSetting.md
ms.openlocfilehash: 42d643faa1b3047c6ee2e3266a68a2ce692ec676
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93449728"
---
# <span data-ttu-id="62238-101">Set-AzureRmServiceFabricSetting</span><span class="sxs-lookup"><span data-stu-id="62238-101">Set-AzureRmServiceFabricSetting</span></span>

## <span data-ttu-id="62238-102">摘要</span><span class="sxs-lookup"><span data-stu-id="62238-102">SYNOPSIS</span></span>
<span data-ttu-id="62238-103">在群集中新增或更新一或多個 Service Fabric 設定。</span><span class="sxs-lookup"><span data-stu-id="62238-103">Add or update one or multiple Service Fabric settings to the cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="62238-104">句法</span><span class="sxs-lookup"><span data-stu-id="62238-104">SYNTAX</span></span>

### <span data-ttu-id="62238-105">OneSetting</span><span class="sxs-lookup"><span data-stu-id="62238-105">OneSetting</span></span>
```
Set-AzureRmServiceFabricSetting [-ResourceGroupName] <String> [-Name] <String> -Section <String>
 -Parameter <String> -Value <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="62238-106">BatchSettings</span><span class="sxs-lookup"><span data-stu-id="62238-106">BatchSettings</span></span>
```
Set-AzureRmServiceFabricSetting [-ResourceGroupName] <String> [-Name] <String>
 -SettingsSectionDescription <PSSettingsSectionDescription[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="62238-107">說明</span><span class="sxs-lookup"><span data-stu-id="62238-107">DESCRIPTION</span></span>
<span data-ttu-id="62238-108">使用 [ **設定] AzureRmServiceFabricSetting** 在群集中新增或更新 Service Fabric 設定。</span><span class="sxs-lookup"><span data-stu-id="62238-108">Use **Set-AzureRmServiceFabricSetting** to add or update Service Fabric settings in a cluster.</span></span>

## <span data-ttu-id="62238-109">示例</span><span class="sxs-lookup"><span data-stu-id="62238-109">EXAMPLES</span></span>

### <span data-ttu-id="62238-110">範例1</span><span class="sxs-lookup"><span data-stu-id="62238-110">Example 1</span></span>
```
PS c:\> Set-AzureRmServiceFabricSetting -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster'  -Section 'NamingService' -Parameter 'MaxFileOperationTimeout' -Value 5000
```

<span data-ttu-id="62238-111">這個命令會將 [MaxFileOperationTimeout] 設定為「NamingService」區段下的值 ' 5000」。</span><span class="sxs-lookup"><span data-stu-id="62238-111">This command will set 'MaxFileOperationTimeout' to value '5000' under the section 'NamingService'.</span></span>

## <span data-ttu-id="62238-112">參數</span><span class="sxs-lookup"><span data-stu-id="62238-112">PARAMETERS</span></span>

### <span data-ttu-id="62238-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62238-113">-DefaultProfile</span></span>
<span data-ttu-id="62238-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="62238-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="62238-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="62238-115">-Name</span></span>
<span data-ttu-id="62238-116">指定群集的名稱。</span><span class="sxs-lookup"><span data-stu-id="62238-116">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="62238-117">-參數</span><span class="sxs-lookup"><span data-stu-id="62238-117">-Parameter</span></span>
<span data-ttu-id="62238-118">參數.</span><span class="sxs-lookup"><span data-stu-id="62238-118">Parameter.</span></span>

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

### <span data-ttu-id="62238-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="62238-119">-ResourceGroupName</span></span>
<span data-ttu-id="62238-120">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="62238-120">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="62238-121">區段</span><span class="sxs-lookup"><span data-stu-id="62238-121">-Section</span></span>
<span data-ttu-id="62238-122">頂部.</span><span class="sxs-lookup"><span data-stu-id="62238-122">Section.</span></span>

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

### <span data-ttu-id="62238-123">-SettingsSectionDescription</span><span class="sxs-lookup"><span data-stu-id="62238-123">-SettingsSectionDescription</span></span>
<span data-ttu-id="62238-124">用戶端驗證類型。</span><span class="sxs-lookup"><span data-stu-id="62238-124">Client authentication type.</span></span>

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

### <span data-ttu-id="62238-125">-值</span><span class="sxs-lookup"><span data-stu-id="62238-125">-Value</span></span>
<span data-ttu-id="62238-126">有效值.</span><span class="sxs-lookup"><span data-stu-id="62238-126">Value.</span></span>

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

### <span data-ttu-id="62238-127">-確認</span><span class="sxs-lookup"><span data-stu-id="62238-127">-Confirm</span></span>
<span data-ttu-id="62238-128">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="62238-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="62238-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="62238-129">-WhatIf</span></span>
<span data-ttu-id="62238-130">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="62238-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="62238-131">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="62238-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="62238-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62238-132">CommonParameters</span></span>
<span data-ttu-id="62238-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="62238-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62238-134">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="62238-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62238-135">輸入</span><span class="sxs-lookup"><span data-stu-id="62238-135">INPUTS</span></span>

### <span data-ttu-id="62238-136">System.object</span><span class="sxs-lookup"><span data-stu-id="62238-136">System.String</span></span>
<span data-ttu-id="62238-137">參數：參數 (ByValue) ，Section (ByValue) ，值 (ByValue) </span><span class="sxs-lookup"><span data-stu-id="62238-137">Parameters: Parameter (ByValue), Section (ByValue), Value (ByValue)</span></span>

### <span data-ttu-id="62238-138">PSSettingsSectionDescription [] 的 ServiceFabric []</span><span class="sxs-lookup"><span data-stu-id="62238-138">Microsoft.Azure.Commands.ServiceFabric.Models.PSSettingsSectionDescription[]</span></span>
<span data-ttu-id="62238-139">參數： SettingsSectionDescription (ByValue) </span><span class="sxs-lookup"><span data-stu-id="62238-139">Parameters: SettingsSectionDescription (ByValue)</span></span>

## <span data-ttu-id="62238-140">輸出</span><span class="sxs-lookup"><span data-stu-id="62238-140">OUTPUTS</span></span>

### <span data-ttu-id="62238-141">PSCluster 中的 ServiceFabric。</span><span class="sxs-lookup"><span data-stu-id="62238-141">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="62238-142">筆記</span><span class="sxs-lookup"><span data-stu-id="62238-142">NOTES</span></span>

## <span data-ttu-id="62238-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="62238-143">RELATED LINKS</span></span>
