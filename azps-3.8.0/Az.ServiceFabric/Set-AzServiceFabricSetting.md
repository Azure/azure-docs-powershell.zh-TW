---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/set-azservicefabricsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Set-AzServiceFabricSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Set-AzServiceFabricSetting.md
ms.openlocfilehash: 10c9c634d1435e9460b72bfd1ccdb7e77f7fea53
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93956537"
---
# <span data-ttu-id="111a5-101">Set-AzServiceFabricSetting</span><span class="sxs-lookup"><span data-stu-id="111a5-101">Set-AzServiceFabricSetting</span></span>

## <span data-ttu-id="111a5-102">摘要</span><span class="sxs-lookup"><span data-stu-id="111a5-102">SYNOPSIS</span></span>
<span data-ttu-id="111a5-103">在群集中新增或更新一或多個 Service Fabric 設定。</span><span class="sxs-lookup"><span data-stu-id="111a5-103">Add or update one or multiple Service Fabric settings to the cluster.</span></span>

## <span data-ttu-id="111a5-104">句法</span><span class="sxs-lookup"><span data-stu-id="111a5-104">SYNTAX</span></span>

### <span data-ttu-id="111a5-105">OneSetting</span><span class="sxs-lookup"><span data-stu-id="111a5-105">OneSetting</span></span>
```
Set-AzServiceFabricSetting [-ResourceGroupName] <String> [-Name] <String> -Section <String> -Parameter <String>
 -Value <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="111a5-106">BatchSettings</span><span class="sxs-lookup"><span data-stu-id="111a5-106">BatchSettings</span></span>
```
Set-AzServiceFabricSetting [-ResourceGroupName] <String> [-Name] <String>
 -SettingsSectionDescription <PSSettingsSectionDescription[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="111a5-107">說明</span><span class="sxs-lookup"><span data-stu-id="111a5-107">DESCRIPTION</span></span>
<span data-ttu-id="111a5-108">使用 [ **設定] AzServiceFabricSetting** 在群集中新增或更新 Service Fabric 設定。</span><span class="sxs-lookup"><span data-stu-id="111a5-108">Use **Set-AzServiceFabricSetting** to add or update Service Fabric settings in a cluster.</span></span>

## <span data-ttu-id="111a5-109">示例</span><span class="sxs-lookup"><span data-stu-id="111a5-109">EXAMPLES</span></span>

### <span data-ttu-id="111a5-110">範例1</span><span class="sxs-lookup"><span data-stu-id="111a5-110">Example 1</span></span>
```
PS c:\> Set-AzServiceFabricSetting -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster'  -Section 'NamingService' -Parameter 'MaxFileOperationTimeout' -Value 5000
```

<span data-ttu-id="111a5-111">這個命令會將 [MaxFileOperationTimeout] 設定為「NamingService」區段下的值 ' 5000」。</span><span class="sxs-lookup"><span data-stu-id="111a5-111">This command will set 'MaxFileOperationTimeout' to value '5000' under the section 'NamingService'.</span></span>

## <span data-ttu-id="111a5-112">參數</span><span class="sxs-lookup"><span data-stu-id="111a5-112">PARAMETERS</span></span>

### <span data-ttu-id="111a5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="111a5-113">-DefaultProfile</span></span>
<span data-ttu-id="111a5-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="111a5-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="111a5-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="111a5-115">-Name</span></span>
<span data-ttu-id="111a5-116">指定群集的名稱</span><span class="sxs-lookup"><span data-stu-id="111a5-116">Specify the name of the cluster</span></span>

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

### <span data-ttu-id="111a5-117">-參數</span><span class="sxs-lookup"><span data-stu-id="111a5-117">-Parameter</span></span>
<span data-ttu-id="111a5-118">結構設定的參數名稱</span><span class="sxs-lookup"><span data-stu-id="111a5-118">Parameter name of the fabric setting</span></span>

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

### <span data-ttu-id="111a5-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="111a5-119">-ResourceGroupName</span></span>
<span data-ttu-id="111a5-120">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="111a5-120">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="111a5-121">區段</span><span class="sxs-lookup"><span data-stu-id="111a5-121">-Section</span></span>
<span data-ttu-id="111a5-122">結構設定的章節名稱</span><span class="sxs-lookup"><span data-stu-id="111a5-122">Section name of the fabric setting</span></span>

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

### <span data-ttu-id="111a5-123">-SettingsSectionDescription</span><span class="sxs-lookup"><span data-stu-id="111a5-123">-SettingsSectionDescription</span></span>
<span data-ttu-id="111a5-124">結構設定陣列</span><span class="sxs-lookup"><span data-stu-id="111a5-124">An array of fabric settings</span></span>

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

### <span data-ttu-id="111a5-125">-值</span><span class="sxs-lookup"><span data-stu-id="111a5-125">-Value</span></span>
<span data-ttu-id="111a5-126">結構設定的參數值</span><span class="sxs-lookup"><span data-stu-id="111a5-126">Parameter value of the fabric setting</span></span>

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

### <span data-ttu-id="111a5-127">-確認</span><span class="sxs-lookup"><span data-stu-id="111a5-127">-Confirm</span></span>
<span data-ttu-id="111a5-128">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="111a5-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="111a5-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="111a5-129">-WhatIf</span></span>
<span data-ttu-id="111a5-130">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="111a5-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="111a5-131">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="111a5-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="111a5-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="111a5-132">CommonParameters</span></span>
<span data-ttu-id="111a5-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="111a5-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="111a5-134">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="111a5-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="111a5-135">輸入</span><span class="sxs-lookup"><span data-stu-id="111a5-135">INPUTS</span></span>

### <span data-ttu-id="111a5-136">System.object</span><span class="sxs-lookup"><span data-stu-id="111a5-136">System.String</span></span>

### <span data-ttu-id="111a5-137">PSSettingsSectionDescription [] 的 ServiceFabric []</span><span class="sxs-lookup"><span data-stu-id="111a5-137">Microsoft.Azure.Commands.ServiceFabric.Models.PSSettingsSectionDescription[]</span></span>

## <span data-ttu-id="111a5-138">輸出</span><span class="sxs-lookup"><span data-stu-id="111a5-138">OUTPUTS</span></span>

### <span data-ttu-id="111a5-139">PSCluster 中的 ServiceFabric。</span><span class="sxs-lookup"><span data-stu-id="111a5-139">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="111a5-140">筆記</span><span class="sxs-lookup"><span data-stu-id="111a5-140">NOTES</span></span>

## <span data-ttu-id="111a5-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="111a5-141">RELATED LINKS</span></span>
