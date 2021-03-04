---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/powershell/module/az.servicefabric/remove-azservicefabricsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricSetting.md
ms.openlocfilehash: 2df7c5f6af50bf581963f08e0544eb453f4b27df
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101915805"
---
# <span data-ttu-id="39df9-101">Remove-AzServiceFabricSetting</span><span class="sxs-lookup"><span data-stu-id="39df9-101">Remove-AzServiceFabricSetting</span></span>

## <span data-ttu-id="39df9-102">簡介</span><span class="sxs-lookup"><span data-stu-id="39df9-102">SYNOPSIS</span></span>
<span data-ttu-id="39df9-103">從組群移除一或多個服務結構設定。</span><span class="sxs-lookup"><span data-stu-id="39df9-103">Remove one or multiple Service Fabric setting from the cluster.</span></span>

## <span data-ttu-id="39df9-104">語法</span><span class="sxs-lookup"><span data-stu-id="39df9-104">SYNTAX</span></span>

### <span data-ttu-id="39df9-105">OneSetting</span><span class="sxs-lookup"><span data-stu-id="39df9-105">OneSetting</span></span>
```
Remove-AzServiceFabricSetting [-ResourceGroupName] <String> [-Name] <String> -Section <String>
 -Parameter <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="39df9-106">BatchSettings</span><span class="sxs-lookup"><span data-stu-id="39df9-106">BatchSettings</span></span>
```
Remove-AzServiceFabricSetting [-ResourceGroupName] <String> [-Name] <String>
 -SettingsSectionDescription <PSSettingsSectionDescription[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="39df9-107">描述</span><span class="sxs-lookup"><span data-stu-id="39df9-107">DESCRIPTION</span></span>
<span data-ttu-id="39df9-108">使用 **Remove-AzServiceFabricSetting** 從組群移除服務佈設定。</span><span class="sxs-lookup"><span data-stu-id="39df9-108">Use **Remove-AzServiceFabricSetting** to remove Service Fabric settings from the cluster.</span></span>

## <span data-ttu-id="39df9-109">例子</span><span class="sxs-lookup"><span data-stu-id="39df9-109">EXAMPLES</span></span>

### <span data-ttu-id="39df9-110">範例 1</span><span class="sxs-lookup"><span data-stu-id="39df9-110">Example 1</span></span>
```
PS c:> Remove-AzServiceFabricSetting -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -Section 'EseStore' -Parameter 'MaxCursors'
```

<span data-ttu-id="39df9-111">此命令會移除在 "EseStore" 區段下的設定 'MaxCursors'。</span><span class="sxs-lookup"><span data-stu-id="39df9-111">This command will remove settings 'MaxCursors' under 'EseStore' section.</span></span>

## <span data-ttu-id="39df9-112">參數</span><span class="sxs-lookup"><span data-stu-id="39df9-112">PARAMETERS</span></span>

### <span data-ttu-id="39df9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39df9-113">-DefaultProfile</span></span>
<span data-ttu-id="39df9-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="39df9-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="39df9-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="39df9-115">-Name</span></span>
<span data-ttu-id="39df9-116">指定組名</span><span class="sxs-lookup"><span data-stu-id="39df9-116">Specify the name of the cluster</span></span>

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

### <span data-ttu-id="39df9-117">-Parameter</span><span class="sxs-lookup"><span data-stu-id="39df9-117">-Parameter</span></span>
<span data-ttu-id="39df9-118">布料設定的參數名稱</span><span class="sxs-lookup"><span data-stu-id="39df9-118">Parameter name of the fabric setting</span></span>

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

### <span data-ttu-id="39df9-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="39df9-119">-ResourceGroupName</span></span>
<span data-ttu-id="39df9-120">指定資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="39df9-120">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="39df9-121">-區段</span><span class="sxs-lookup"><span data-stu-id="39df9-121">-Section</span></span>
<span data-ttu-id="39df9-122">布料設定區段名稱</span><span class="sxs-lookup"><span data-stu-id="39df9-122">Section name of the fabric setting</span></span>

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

### <span data-ttu-id="39df9-123">-SettingsSectionDescription</span><span class="sxs-lookup"><span data-stu-id="39df9-123">-SettingsSectionDescription</span></span>
<span data-ttu-id="39df9-124">布料設定陣列</span><span class="sxs-lookup"><span data-stu-id="39df9-124">An array of fabric settings</span></span>

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

### <span data-ttu-id="39df9-125">-確認</span><span class="sxs-lookup"><span data-stu-id="39df9-125">-Confirm</span></span>
<span data-ttu-id="39df9-126">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="39df9-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="39df9-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="39df9-127">-WhatIf</span></span>
<span data-ttu-id="39df9-128">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="39df9-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="39df9-129">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="39df9-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="39df9-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39df9-130">CommonParameters</span></span>
<span data-ttu-id="39df9-131">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="39df9-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39df9-132">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="39df9-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39df9-133">輸入</span><span class="sxs-lookup"><span data-stu-id="39df9-133">INPUTS</span></span>

### <span data-ttu-id="39df9-134">System.String</span><span class="sxs-lookup"><span data-stu-id="39df9-134">System.String</span></span>

### <span data-ttu-id="39df9-135">Microsoft.Azure.Commands.ServiceFabric.Models.PSSettingsSectionDescription[]</span><span class="sxs-lookup"><span data-stu-id="39df9-135">Microsoft.Azure.Commands.ServiceFabric.Models.PSSettingsSectionDescription[]</span></span>

## <span data-ttu-id="39df9-136">輸出</span><span class="sxs-lookup"><span data-stu-id="39df9-136">OUTPUTS</span></span>

### <span data-ttu-id="39df9-137">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span><span class="sxs-lookup"><span data-stu-id="39df9-137">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="39df9-138">筆記</span><span class="sxs-lookup"><span data-stu-id="39df9-138">NOTES</span></span>

## <span data-ttu-id="39df9-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="39df9-139">RELATED LINKS</span></span>
