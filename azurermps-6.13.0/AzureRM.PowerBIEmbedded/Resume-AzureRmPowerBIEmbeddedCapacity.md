---
external help file: Microsoft.Azure.Commands.PowerBI.dll-Help.xml
Module Name: AzureRM.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.powerbiembedded/resume-azurermpowerbiembeddedcapacity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.PowerBI/help/Resume-AzureRmPowerBIEmbeddedCapacity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.PowerBI/help/Resume-AzureRmPowerBIEmbeddedCapacity.md
ms.openlocfilehash: 29113eecc02443fe2fbc8f57ada1fcfa8e7a2d98
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93447293"
---
# <span data-ttu-id="185ae-101">Resume-AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="185ae-101">Resume-AzureRmPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="185ae-102">摘要</span><span class="sxs-lookup"><span data-stu-id="185ae-102">SYNOPSIS</span></span>
<span data-ttu-id="185ae-103">簡歷 PowerBI 內嵌容量的實例。</span><span class="sxs-lookup"><span data-stu-id="185ae-103">Resumes an instance of PowerBI Embedded Capacity.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="185ae-104">句法</span><span class="sxs-lookup"><span data-stu-id="185ae-104">SYNTAX</span></span>

### <span data-ttu-id="185ae-105">ByNameAndResourceGroup (預設) </span><span class="sxs-lookup"><span data-stu-id="185ae-105">ByNameAndResourceGroup (Default)</span></span>
```
Resume-AzureRmPowerBIEmbeddedCapacity [-Name] <String> [-ResourceGroupName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="185ae-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="185ae-106">ByResourceId</span></span>
```
Resume-AzureRmPowerBIEmbeddedCapacity [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="185ae-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="185ae-107">ByInputObject</span></span>
```
Resume-AzureRmPowerBIEmbeddedCapacity [-InputObject] <PSPowerBIEmbeddedCapacity> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="185ae-108">說明</span><span class="sxs-lookup"><span data-stu-id="185ae-108">DESCRIPTION</span></span>
<span data-ttu-id="185ae-109">Resume-AzureRmPowerBIEmbeddedCapacity Cmdlet 會繼續執行 PowerBI 內嵌容量的實例</span><span class="sxs-lookup"><span data-stu-id="185ae-109">The Resume-AzureRmPowerBIEmbeddedCapacity cmdlet resumes an instance of PowerBI Embedded Capacity</span></span>

## <span data-ttu-id="185ae-110">示例</span><span class="sxs-lookup"><span data-stu-id="185ae-110">EXAMPLES</span></span>

### <span data-ttu-id="185ae-111">範例1</span><span class="sxs-lookup"><span data-stu-id="185ae-111">Example 1</span></span>
```
PS C:\> Resume-AzureRmPowerBIEmbeddedCapacity -Name "testcapacity" -ResourceGroupName "testRG" -PassThru
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

<span data-ttu-id="185ae-112">這個命令會在 resourcegroup testRG 中繼續已有名為 testcapacity 的暫停容量</span><span class="sxs-lookup"><span data-stu-id="185ae-112">This command will resume a paused capacity named testcapacity in the resourcegroup testRG</span></span>

## <span data-ttu-id="185ae-113">參數</span><span class="sxs-lookup"><span data-stu-id="185ae-113">PARAMETERS</span></span>

### <span data-ttu-id="185ae-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="185ae-114">-DefaultProfile</span></span>
<span data-ttu-id="185ae-115">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="185ae-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="185ae-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="185ae-116">-InputObject</span></span>
<span data-ttu-id="185ae-117">管道的輸入物件</span><span class="sxs-lookup"><span data-stu-id="185ae-117">Input object for Piping</span></span>

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

### <span data-ttu-id="185ae-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="185ae-118">-Name</span></span>
<span data-ttu-id="185ae-119">PowerBI 內嵌容量的名稱</span><span class="sxs-lookup"><span data-stu-id="185ae-119">Name of the PowerBI Embedded Capacity</span></span>

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

### <span data-ttu-id="185ae-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="185ae-120">-PassThru</span></span>
<span data-ttu-id="185ae-121">{{Fill PassThru 描述}}</span><span class="sxs-lookup"><span data-stu-id="185ae-121">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="185ae-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="185ae-122">-ResourceGroupName</span></span>
<span data-ttu-id="185ae-123">容量所屬之 Azure 資源群組的名稱</span><span class="sxs-lookup"><span data-stu-id="185ae-123">Name of the Azure resource group to which the capacity belongs</span></span>

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

### <span data-ttu-id="185ae-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="185ae-124">-ResourceId</span></span>
<span data-ttu-id="185ae-125">Azure 資源識別碼</span><span class="sxs-lookup"><span data-stu-id="185ae-125">Azure resource ID</span></span>

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

### <span data-ttu-id="185ae-126">-確認</span><span class="sxs-lookup"><span data-stu-id="185ae-126">-Confirm</span></span>
<span data-ttu-id="185ae-127">提示使用者確認是否要執行該作業</span><span class="sxs-lookup"><span data-stu-id="185ae-127">Prompts user to confirm whether to perform the operation</span></span>

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

### <span data-ttu-id="185ae-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="185ae-128">-WhatIf</span></span>
<span data-ttu-id="185ae-129">描述目前操作將執行但不會實際執行的動作</span><span class="sxs-lookup"><span data-stu-id="185ae-129">Describes the actions the current operation will perform without actually performing them</span></span>

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

### <span data-ttu-id="185ae-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="185ae-130">CommonParameters</span></span>
<span data-ttu-id="185ae-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="185ae-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="185ae-132">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="185ae-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="185ae-133">輸入</span><span class="sxs-lookup"><span data-stu-id="185ae-133">INPUTS</span></span>

### <span data-ttu-id="185ae-134">System.object</span><span class="sxs-lookup"><span data-stu-id="185ae-134">System.String</span></span>

### <span data-ttu-id="185ae-135">[PSPowerBIEmbeddedCapacity] 命令。</span><span class="sxs-lookup"><span data-stu-id="185ae-135">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>
<span data-ttu-id="185ae-136">參數： InputObject (ByValue) </span><span class="sxs-lookup"><span data-stu-id="185ae-136">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="185ae-137">輸出</span><span class="sxs-lookup"><span data-stu-id="185ae-137">OUTPUTS</span></span>

### <span data-ttu-id="185ae-138">[PSPowerBIEmbeddedCapacity] 命令。</span><span class="sxs-lookup"><span data-stu-id="185ae-138">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="185ae-139">筆記</span><span class="sxs-lookup"><span data-stu-id="185ae-139">NOTES</span></span>

## <span data-ttu-id="185ae-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="185ae-140">RELATED LINKS</span></span>

[<span data-ttu-id="185ae-141">AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="185ae-141">Get-AzureRmPowerBIEmbeddedCapacity</span></span>](./Get-AzureRmPowerBIEmbeddedCapacity.md)

[<span data-ttu-id="185ae-142">暫停-AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="185ae-142">Suspend-AzureRmPowerBIEmbeddedCapacity</span></span>](./Suspend-AzureRmPowerBIEmbeddedCapacity.md)
