---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PowerBI.dll-Help.xml
Module Name: Az.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/powershell/module/az.powerbiembedded/suspend-azpowerbiembeddedcapacity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Suspend-AzPowerBIEmbeddedCapacity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Suspend-AzPowerBIEmbeddedCapacity.md
ms.openlocfilehash: 54c546ed7bac74a13030a9ca2f18276761e2d381
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101912626"
---
# <span data-ttu-id="971d0-101">Suspend-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="971d0-101">Suspend-AzPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="971d0-102">簡介</span><span class="sxs-lookup"><span data-stu-id="971d0-102">SYNOPSIS</span></span>
<span data-ttu-id="971d0-103">暫停 PowerBI 內嵌容量的實例。</span><span class="sxs-lookup"><span data-stu-id="971d0-103">Suspends an instance of PowerBI Embedded Capacity.</span></span>

## <span data-ttu-id="971d0-104">語法</span><span class="sxs-lookup"><span data-stu-id="971d0-104">SYNTAX</span></span>

### <span data-ttu-id="971d0-105">ByNameAndResourceGroup (預設) </span><span class="sxs-lookup"><span data-stu-id="971d0-105">ByNameAndResourceGroup (Default)</span></span>
```
Suspend-AzPowerBIEmbeddedCapacity [-Name] <String> [-ResourceGroupName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="971d0-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="971d0-106">ByResourceId</span></span>
```
Suspend-AzPowerBIEmbeddedCapacity [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="971d0-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="971d0-107">ByInputObject</span></span>
```
Suspend-AzPowerBIEmbeddedCapacity [-InputObject] <PSPowerBIEmbeddedCapacity> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="971d0-108">描述</span><span class="sxs-lookup"><span data-stu-id="971d0-108">DESCRIPTION</span></span>
<span data-ttu-id="971d0-109">此Suspend-AzPowerBIEmbeddedCapacity Cmdlet 會暫停 PowerBI 內嵌容量實例</span><span class="sxs-lookup"><span data-stu-id="971d0-109">The Suspend-AzPowerBIEmbeddedCapacity cmdlet suspends an instance of PowerBI Embedded Capacity</span></span>

## <span data-ttu-id="971d0-110">例子</span><span class="sxs-lookup"><span data-stu-id="971d0-110">EXAMPLES</span></span>

### <span data-ttu-id="971d0-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="971d0-111">Example 1</span></span>
```
PS C:\> Suspend-AzPowerBIEmbeddedCapacity -Name "testcapacity" -ResourceGroupName "testRG" -PassThru
Type                   : Microsoft.PowerBIDedicated/capacities
Id                     : /subscriptions/78e47976-.../resourceGroups/testRG/providers/Microsoft.PowerBIDedicated/capacities/testcapacity
ResourceGroup          : testRG
Name                   : testcapacity
Location               : West Central US
State                  : Paused
Administrator          : {admin@microsoft.com}
Sku                    : A1
Tier                   : PBIE_Azure
Tag                    : {}
```

<span data-ttu-id="971d0-112">此命令會暫停資源組測試組中名為 test活取的活動容量</span><span class="sxs-lookup"><span data-stu-id="971d0-112">This command will suspend an active capacity named testcapacity in the resourcegroup testgroup</span></span>

## <span data-ttu-id="971d0-113">參數</span><span class="sxs-lookup"><span data-stu-id="971d0-113">PARAMETERS</span></span>

### <span data-ttu-id="971d0-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="971d0-114">-DefaultProfile</span></span>
<span data-ttu-id="971d0-115">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="971d0-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="971d0-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="971d0-116">-InputObject</span></span>
<span data-ttu-id="971d0-117">用於管線的輸入物件</span><span class="sxs-lookup"><span data-stu-id="971d0-117">Input object for Piping</span></span>

```yaml
Type: Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="971d0-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="971d0-118">-Name</span></span>
<span data-ttu-id="971d0-119">PowerBI 內嵌容量的名稱</span><span class="sxs-lookup"><span data-stu-id="971d0-119">Name of the PowerBI Embedded Capacity</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameAndResourceGroup
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="971d0-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="971d0-120">-PassThru</span></span>
<span data-ttu-id="971d0-121">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="971d0-121">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="971d0-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="971d0-122">-ResourceGroupName</span></span>
<span data-ttu-id="971d0-123">容量所屬的 Azure 資源組名</span><span class="sxs-lookup"><span data-stu-id="971d0-123">Name of the Azure resource group to which the capacity belongs</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameAndResourceGroup
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="971d0-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="971d0-124">-ResourceId</span></span>
<span data-ttu-id="971d0-125">Azure 資源識別碼</span><span class="sxs-lookup"><span data-stu-id="971d0-125">Azure resource ID</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="971d0-126">-確認</span><span class="sxs-lookup"><span data-stu-id="971d0-126">-Confirm</span></span>
<span data-ttu-id="971d0-127">提示使用者確認是否要執行作業</span><span class="sxs-lookup"><span data-stu-id="971d0-127">Prompts user to confirm whether to perform the operation</span></span>

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

### <span data-ttu-id="971d0-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="971d0-128">-WhatIf</span></span>
<span data-ttu-id="971d0-129">說明目前作業不會實際執行的動作</span><span class="sxs-lookup"><span data-stu-id="971d0-129">Describes the actions the current operation will perform without actually performing them</span></span>

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

### <span data-ttu-id="971d0-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="971d0-130">CommonParameters</span></span>
<span data-ttu-id="971d0-131">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="971d0-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="971d0-132">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="971d0-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="971d0-133">輸入</span><span class="sxs-lookup"><span data-stu-id="971d0-133">INPUTS</span></span>

### <span data-ttu-id="971d0-134">System.String</span><span class="sxs-lookup"><span data-stu-id="971d0-134">System.String</span></span>

### <span data-ttu-id="971d0-135">Microsoft.Azure.Commands.PowerBI.models.PSPowerBIEmbeddedSoft</span><span class="sxs-lookup"><span data-stu-id="971d0-135">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="971d0-136">輸出</span><span class="sxs-lookup"><span data-stu-id="971d0-136">OUTPUTS</span></span>

### <span data-ttu-id="971d0-137">Microsoft.Azure.Commands.PowerBI.models.PSPowerBIEmbeddedSoft</span><span class="sxs-lookup"><span data-stu-id="971d0-137">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="971d0-138">筆記</span><span class="sxs-lookup"><span data-stu-id="971d0-138">NOTES</span></span>

## <span data-ttu-id="971d0-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="971d0-139">RELATED LINKS</span></span>

[<span data-ttu-id="971d0-140">Get-AzPowerBIEmbedded一切</span><span class="sxs-lookup"><span data-stu-id="971d0-140">Get-AzPowerBIEmbeddedCapacity</span></span>](./Get-AzPowerBIEmbeddedCapacity.md)

[<span data-ttu-id="971d0-141">Resume-AzPowerBIEmbedded可說</span><span class="sxs-lookup"><span data-stu-id="971d0-141">Resume-AzPowerBIEmbeddedCapacity</span></span>](./Resume-AzPowerBIEmbeddedCapacity.md)

