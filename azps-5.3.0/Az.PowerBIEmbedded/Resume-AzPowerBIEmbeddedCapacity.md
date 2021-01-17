---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PowerBI.dll-Help.xml
Module Name: Az.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/en-us/powershell/module/az.powerbiembedded/resume-azpowerbiembeddedcapacity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Resume-AzPowerBIEmbeddedCapacity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Resume-AzPowerBIEmbeddedCapacity.md
ms.openlocfilehash: 4fdb8845b59a57b20813f92e3858cc7c54310d23
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98437407"
---
# <span data-ttu-id="3fa51-101">Resume-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="3fa51-101">Resume-AzPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="3fa51-102">摘要</span><span class="sxs-lookup"><span data-stu-id="3fa51-102">SYNOPSIS</span></span>
<span data-ttu-id="3fa51-103">簡歷 PowerBI 內嵌容量的實例。</span><span class="sxs-lookup"><span data-stu-id="3fa51-103">Resumes an instance of PowerBI Embedded Capacity.</span></span>

## <span data-ttu-id="3fa51-104">句法</span><span class="sxs-lookup"><span data-stu-id="3fa51-104">SYNTAX</span></span>

### <span data-ttu-id="3fa51-105">ByNameAndResourceGroup (預設) </span><span class="sxs-lookup"><span data-stu-id="3fa51-105">ByNameAndResourceGroup (Default)</span></span>
```
Resume-AzPowerBIEmbeddedCapacity [-Name] <String> [-ResourceGroupName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3fa51-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="3fa51-106">ByResourceId</span></span>
```
Resume-AzPowerBIEmbeddedCapacity [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3fa51-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="3fa51-107">ByInputObject</span></span>
```
Resume-AzPowerBIEmbeddedCapacity [-InputObject] <PSPowerBIEmbeddedCapacity> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3fa51-108">說明</span><span class="sxs-lookup"><span data-stu-id="3fa51-108">DESCRIPTION</span></span>
<span data-ttu-id="3fa51-109">Resume-AzPowerBIEmbeddedCapacity Cmdlet 會繼續執行 PowerBI 內嵌容量的實例</span><span class="sxs-lookup"><span data-stu-id="3fa51-109">The Resume-AzPowerBIEmbeddedCapacity cmdlet resumes an instance of PowerBI Embedded Capacity</span></span>

## <span data-ttu-id="3fa51-110">示例</span><span class="sxs-lookup"><span data-stu-id="3fa51-110">EXAMPLES</span></span>

### <span data-ttu-id="3fa51-111">範例1</span><span class="sxs-lookup"><span data-stu-id="3fa51-111">Example 1</span></span>
```
PS C:\> Resume-AzPowerBIEmbeddedCapacity -Name "testcapacity" -ResourceGroupName "testRG" -PassThru
Type                   : Microsoft.PowerBIDedicated/capacities
Id                     : /subscriptions/78e47976-.../resourceGroups/testRG/providers/Microsoft.PowerBIDedicated/capacities/testcapacity
ResourceGroup          : testRG
Name                   : testcapacity
Location               : West Central US
State                  : Succeeded
Administrator          : {admin@microsoft.com}
Sku                    : A1
Tier                   : PBIE_Azure
Tag                    : {}
```

<span data-ttu-id="3fa51-112">這個命令會在 resourcegroup testRG 中繼續已有名為 testcapacity 的暫停容量</span><span class="sxs-lookup"><span data-stu-id="3fa51-112">This command will resume a paused capacity named testcapacity in the resourcegroup testRG</span></span>

## <span data-ttu-id="3fa51-113">參數</span><span class="sxs-lookup"><span data-stu-id="3fa51-113">PARAMETERS</span></span>

### <span data-ttu-id="3fa51-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3fa51-114">-DefaultProfile</span></span>
<span data-ttu-id="3fa51-115">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="3fa51-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3fa51-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3fa51-116">-InputObject</span></span>
<span data-ttu-id="3fa51-117">管道的輸入物件</span><span class="sxs-lookup"><span data-stu-id="3fa51-117">Input object for Piping</span></span>

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

### <span data-ttu-id="3fa51-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="3fa51-118">-Name</span></span>
<span data-ttu-id="3fa51-119">PowerBI 內嵌容量的名稱</span><span class="sxs-lookup"><span data-stu-id="3fa51-119">Name of the PowerBI Embedded Capacity</span></span>

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

### <span data-ttu-id="3fa51-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3fa51-120">-PassThru</span></span>
<span data-ttu-id="3fa51-121">{{Fill PassThru 描述}}</span><span class="sxs-lookup"><span data-stu-id="3fa51-121">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="3fa51-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3fa51-122">-ResourceGroupName</span></span>
<span data-ttu-id="3fa51-123">容量所屬之 Azure 資源群組的名稱</span><span class="sxs-lookup"><span data-stu-id="3fa51-123">Name of the Azure resource group to which the capacity belongs</span></span>

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

### <span data-ttu-id="3fa51-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3fa51-124">-ResourceId</span></span>
<span data-ttu-id="3fa51-125">Azure 資源識別碼</span><span class="sxs-lookup"><span data-stu-id="3fa51-125">Azure resource ID</span></span>

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

### <span data-ttu-id="3fa51-126">-確認</span><span class="sxs-lookup"><span data-stu-id="3fa51-126">-Confirm</span></span>
<span data-ttu-id="3fa51-127">提示使用者確認是否要執行該作業</span><span class="sxs-lookup"><span data-stu-id="3fa51-127">Prompts user to confirm whether to perform the operation</span></span>

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

### <span data-ttu-id="3fa51-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3fa51-128">-WhatIf</span></span>
<span data-ttu-id="3fa51-129">描述目前操作將執行但不會實際執行的動作</span><span class="sxs-lookup"><span data-stu-id="3fa51-129">Describes the actions the current operation will perform without actually performing them</span></span>

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

### <span data-ttu-id="3fa51-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3fa51-130">CommonParameters</span></span>
<span data-ttu-id="3fa51-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="3fa51-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3fa51-132">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="3fa51-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3fa51-133">輸入</span><span class="sxs-lookup"><span data-stu-id="3fa51-133">INPUTS</span></span>

### <span data-ttu-id="3fa51-134">System.object</span><span class="sxs-lookup"><span data-stu-id="3fa51-134">System.String</span></span>

### <span data-ttu-id="3fa51-135">[PSPowerBIEmbeddedCapacity] 命令。</span><span class="sxs-lookup"><span data-stu-id="3fa51-135">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="3fa51-136">輸出</span><span class="sxs-lookup"><span data-stu-id="3fa51-136">OUTPUTS</span></span>

### <span data-ttu-id="3fa51-137">[PSPowerBIEmbeddedCapacity] 命令。</span><span class="sxs-lookup"><span data-stu-id="3fa51-137">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="3fa51-138">筆記</span><span class="sxs-lookup"><span data-stu-id="3fa51-138">NOTES</span></span>

## <span data-ttu-id="3fa51-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="3fa51-139">RELATED LINKS</span></span>

[<span data-ttu-id="3fa51-140">AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="3fa51-140">Get-AzPowerBIEmbeddedCapacity</span></span>](./Get-AzPowerBIEmbeddedCapacity.md)

[<span data-ttu-id="3fa51-141">暫停-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="3fa51-141">Suspend-AzPowerBIEmbeddedCapacity</span></span>](./Suspend-AzPowerBIEmbeddedCapacity.md)
