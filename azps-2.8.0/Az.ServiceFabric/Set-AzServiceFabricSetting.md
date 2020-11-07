---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/set-azservicefabricsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Set-AzServiceFabricSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Set-AzServiceFabricSetting.md
ms.openlocfilehash: 36371899f1ac8c20bedf8a97bbf262d4df05fa12
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93792067"
---
# <span data-ttu-id="22600-101">Set-AzServiceFabricSetting</span><span class="sxs-lookup"><span data-stu-id="22600-101">Set-AzServiceFabricSetting</span></span>

## <span data-ttu-id="22600-102">摘要</span><span class="sxs-lookup"><span data-stu-id="22600-102">SYNOPSIS</span></span>
<span data-ttu-id="22600-103">在群集中新增或更新一或多個 Service Fabric 設定。</span><span class="sxs-lookup"><span data-stu-id="22600-103">Add or update one or multiple Service Fabric settings to the cluster.</span></span>

## <span data-ttu-id="22600-104">句法</span><span class="sxs-lookup"><span data-stu-id="22600-104">SYNTAX</span></span>

### <span data-ttu-id="22600-105">OneSetting</span><span class="sxs-lookup"><span data-stu-id="22600-105">OneSetting</span></span>
```
Set-AzServiceFabricSetting [-ResourceGroupName] <String> [-Name] <String> -Section <String> -Parameter <String>
 -Value <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="22600-106">BatchSettings</span><span class="sxs-lookup"><span data-stu-id="22600-106">BatchSettings</span></span>
```
Set-AzServiceFabricSetting [-ResourceGroupName] <String> [-Name] <String>
 -SettingsSectionDescription <PSSettingsSectionDescription[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="22600-107">說明</span><span class="sxs-lookup"><span data-stu-id="22600-107">DESCRIPTION</span></span>
<span data-ttu-id="22600-108">使用 [ **設定] AzServiceFabricSetting** 在群集中新增或更新 Service Fabric 設定。</span><span class="sxs-lookup"><span data-stu-id="22600-108">Use **Set-AzServiceFabricSetting** to add or update Service Fabric settings in a cluster.</span></span>

## <span data-ttu-id="22600-109">示例</span><span class="sxs-lookup"><span data-stu-id="22600-109">EXAMPLES</span></span>

### <span data-ttu-id="22600-110">範例1</span><span class="sxs-lookup"><span data-stu-id="22600-110">Example 1</span></span>
```
PS c:\> Set-AzServiceFabricSetting -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster'  -Section 'NamingService' -Parameter 'MaxFileOperationTimeout' -Value 5000
```

<span data-ttu-id="22600-111">這個命令會將 [MaxFileOperationTimeout] 設定為「NamingService」區段下的值 ' 5000」。</span><span class="sxs-lookup"><span data-stu-id="22600-111">This command will set 'MaxFileOperationTimeout' to value '5000' under the section 'NamingService'.</span></span>

## <span data-ttu-id="22600-112">參數</span><span class="sxs-lookup"><span data-stu-id="22600-112">PARAMETERS</span></span>

### <span data-ttu-id="22600-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22600-113">-DefaultProfile</span></span>
<span data-ttu-id="22600-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="22600-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="22600-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="22600-115">-Name</span></span>
<span data-ttu-id="22600-116">指定群集的名稱</span><span class="sxs-lookup"><span data-stu-id="22600-116">Specify the name of the cluster</span></span>

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

### <span data-ttu-id="22600-117">-參數</span><span class="sxs-lookup"><span data-stu-id="22600-117">-Parameter</span></span>
<span data-ttu-id="22600-118">結構設定的參數名稱</span><span class="sxs-lookup"><span data-stu-id="22600-118">Parameter name of the fabric setting</span></span>

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

### <span data-ttu-id="22600-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="22600-119">-ResourceGroupName</span></span>
<span data-ttu-id="22600-120">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="22600-120">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="22600-121">區段</span><span class="sxs-lookup"><span data-stu-id="22600-121">-Section</span></span>
<span data-ttu-id="22600-122">結構設定的章節名稱</span><span class="sxs-lookup"><span data-stu-id="22600-122">Section name of the fabric setting</span></span>

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

### <span data-ttu-id="22600-123">-SettingsSectionDescription</span><span class="sxs-lookup"><span data-stu-id="22600-123">-SettingsSectionDescription</span></span>
<span data-ttu-id="22600-124">結構設定陣列</span><span class="sxs-lookup"><span data-stu-id="22600-124">An array of fabric settings</span></span>

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

### <span data-ttu-id="22600-125">-值</span><span class="sxs-lookup"><span data-stu-id="22600-125">-Value</span></span>
<span data-ttu-id="22600-126">結構設定的參數值</span><span class="sxs-lookup"><span data-stu-id="22600-126">Parameter value of the fabric setting</span></span>

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

### <span data-ttu-id="22600-127">-確認</span><span class="sxs-lookup"><span data-stu-id="22600-127">-Confirm</span></span>
<span data-ttu-id="22600-128">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="22600-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="22600-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="22600-129">-WhatIf</span></span>
<span data-ttu-id="22600-130">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="22600-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="22600-131">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="22600-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="22600-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22600-132">CommonParameters</span></span>
<span data-ttu-id="22600-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="22600-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22600-134">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="22600-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22600-135">輸入</span><span class="sxs-lookup"><span data-stu-id="22600-135">INPUTS</span></span>

### <span data-ttu-id="22600-136">System.object</span><span class="sxs-lookup"><span data-stu-id="22600-136">System.String</span></span>

### <span data-ttu-id="22600-137">PSSettingsSectionDescription [] 的 ServiceFabric []</span><span class="sxs-lookup"><span data-stu-id="22600-137">Microsoft.Azure.Commands.ServiceFabric.Models.PSSettingsSectionDescription[]</span></span>

## <span data-ttu-id="22600-138">輸出</span><span class="sxs-lookup"><span data-stu-id="22600-138">OUTPUTS</span></span>

### <span data-ttu-id="22600-139">PSCluster 中的 ServiceFabric。</span><span class="sxs-lookup"><span data-stu-id="22600-139">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="22600-140">筆記</span><span class="sxs-lookup"><span data-stu-id="22600-140">NOTES</span></span>

## <span data-ttu-id="22600-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="22600-141">RELATED LINKS</span></span>
