---
external help file: Microsoft.Azure.Commands.PowerBI.dll-Help.xml
Module Name: AzureRM.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.powerbiembedded/resume-azurermpowerbiembeddedcapacity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.PowerBI/help/Resume-AzureRmPowerBIEmbeddedCapacity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.PowerBI/help/Resume-AzureRmPowerBIEmbeddedCapacity.md
ms.openlocfilehash: fe660d200c578d15fe8e23e7bfffc9a249651ae2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93444480"
---
# <span data-ttu-id="d19e6-101">Resume-AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="d19e6-101">Resume-AzureRmPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="d19e6-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d19e6-102">SYNOPSIS</span></span>
<span data-ttu-id="d19e6-103">簡歷 PowerBI 內嵌容量的實例。</span><span class="sxs-lookup"><span data-stu-id="d19e6-103">Resumes an instance of PowerBI Embedded Capacity.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d19e6-104">句法</span><span class="sxs-lookup"><span data-stu-id="d19e6-104">SYNTAX</span></span>

```
Resume-AzureRmPowerBIEmbeddedCapacity 
    [-Name] <String> 
    [[-ResourceGroupName] <String>] 
    [-PassThru] 
    [-WhatIf]
    [-Confirm] 
    [<CommonParameters>]
```

## <span data-ttu-id="d19e6-105">說明</span><span class="sxs-lookup"><span data-stu-id="d19e6-105">DESCRIPTION</span></span>
<span data-ttu-id="d19e6-106">Resume-AzureRmPowerBIEmbeddedCapacity Cmdlet 會繼續執行 PowerBI 內嵌容量的實例</span><span class="sxs-lookup"><span data-stu-id="d19e6-106">The Resume-AzureRmPowerBIEmbeddedCapacity cmdlet resumes an instance of PowerBI Embedded Capacity</span></span>

## <span data-ttu-id="d19e6-107">示例</span><span class="sxs-lookup"><span data-stu-id="d19e6-107">EXAMPLES</span></span>

### <span data-ttu-id="d19e6-108">範例1</span><span class="sxs-lookup"><span data-stu-id="d19e6-108">Example 1</span></span>
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

<span data-ttu-id="d19e6-109">這個命令會在 resourcegroup testRG 中繼續已有名為 testcapacity 的暫停容量</span><span class="sxs-lookup"><span data-stu-id="d19e6-109">This command will resume a paused capacity named testcapacity in the resourcegroup testRG</span></span>

## <span data-ttu-id="d19e6-110">參數</span><span class="sxs-lookup"><span data-stu-id="d19e6-110">PARAMETERS</span></span>

### <span data-ttu-id="d19e6-111">-名稱</span><span class="sxs-lookup"><span data-stu-id="d19e6-111">-Name</span></span>
<span data-ttu-id="d19e6-112">PowerBI 內嵌容量的名稱</span><span class="sxs-lookup"><span data-stu-id="d19e6-112">Name of the PowerBI Embedded Capacity</span></span>

```yaml
Type: String
Parameter Sets: ByNameAndResourceGroup
Aliases: 

Required: True
Position: 0
Default value: None
Accept wildcard characters: False
```

### <span data-ttu-id="d19e6-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d19e6-113">-ResourceGroupName</span></span>
<span data-ttu-id="d19e6-114">容量所屬之 Azure 資源群組的名稱</span><span class="sxs-lookup"><span data-stu-id="d19e6-114">Name of the Azure resource group to which the capacity belongs</span></span>

```yaml
Type: String
Parameter Sets: ByNameAndResourceGroup
Aliases: 

Required: False
Default value: None
Accept wildcard characters: False
```

### <span data-ttu-id="d19e6-115">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d19e6-115">-ResourceId</span></span>
<span data-ttu-id="d19e6-116">Azure 資源識別碼</span><span class="sxs-lookup"><span data-stu-id="d19e6-116">Azure resource ID</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d19e6-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d19e6-117">-InputObject</span></span>
<span data-ttu-id="d19e6-118">管道的輸入物件</span><span class="sxs-lookup"><span data-stu-id="d19e6-118">Input object for Piping</span></span>

```yaml
Type: PSPowerBIEmbeddedCapacity
Parameter Sets: ByInputObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d19e6-119">-確認</span><span class="sxs-lookup"><span data-stu-id="d19e6-119">-Confirm</span></span>
<span data-ttu-id="d19e6-120">提示使用者確認是否要執行該作業</span><span class="sxs-lookup"><span data-stu-id="d19e6-120">Prompts user to confirm whether to perform the operation</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d19e6-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d19e6-121">-WhatIf</span></span>
<span data-ttu-id="d19e6-122">描述目前操作將執行但不會實際執行的動作</span><span class="sxs-lookup"><span data-stu-id="d19e6-122">Describes the actions the current operation will perform without actually performing them</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d19e6-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d19e6-123">CommonParameters</span></span>
<span data-ttu-id="d19e6-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d19e6-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d19e6-125">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="d19e6-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d19e6-126">輸入</span><span class="sxs-lookup"><span data-stu-id="d19e6-126">INPUTS</span></span>

### <span data-ttu-id="d19e6-127">所有</span><span class="sxs-lookup"><span data-stu-id="d19e6-127">None</span></span>
<span data-ttu-id="d19e6-128">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="d19e6-128">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="d19e6-129">輸出</span><span class="sxs-lookup"><span data-stu-id="d19e6-129">OUTPUTS</span></span>

### <span data-ttu-id="d19e6-130">[PSPowerBIEmbeddedCapacity] 命令。</span><span class="sxs-lookup"><span data-stu-id="d19e6-130">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="d19e6-131">筆記</span><span class="sxs-lookup"><span data-stu-id="d19e6-131">NOTES</span></span>

## <span data-ttu-id="d19e6-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="d19e6-132">RELATED LINKS</span></span>

[<span data-ttu-id="d19e6-133">AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="d19e6-133">Get-AzureRmPowerBIEmbeddedCapacity</span></span>](./Get-AzureRmPowerBIEmbeddedCapacity.md)

[<span data-ttu-id="d19e6-134">暫停-AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="d19e6-134">Suspend-AzureRmPowerBIEmbeddedCapacity</span></span>](./Suspend-AzureRmPowerBIEmbeddedCapacity.md)
