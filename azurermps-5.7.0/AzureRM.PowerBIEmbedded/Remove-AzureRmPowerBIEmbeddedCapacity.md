---
external help file: Microsoft.Azure.Commands.PowerBI.dll-Help.xml
Module Name: AzureRM.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.powerbiembedded/remove-azurermpowerbiembeddedcapacity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.PowerBI/help/Remove-AzureRmPowerBIEmbeddedCapacity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.PowerBI/help/Remove-AzureRmPowerBIEmbeddedCapacity.md
ms.openlocfilehash: bbdfe43b4f6cad72432c85876c71bcd34a9a371c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93624700"
---
# <span data-ttu-id="2ef39-101">Remove-AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="2ef39-101">Remove-AzureRmPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="2ef39-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2ef39-102">SYNOPSIS</span></span>
<span data-ttu-id="2ef39-103">刪除 PowerBI 內嵌容量的實例。</span><span class="sxs-lookup"><span data-stu-id="2ef39-103">Deletes an instance of PowerBI Embedded Capacity.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2ef39-104">句法</span><span class="sxs-lookup"><span data-stu-id="2ef39-104">SYNTAX</span></span>

```
Remove-AzureRmPowerBIEmbeddedCapacity 
    [-Name] <String> 
    [[-ResourceGroupName] <String>] 
    [-PassThru] 
    [-WhatIf]
    [-Confirm] 
    [<CommonParameters>]
```

## <span data-ttu-id="2ef39-105">說明</span><span class="sxs-lookup"><span data-stu-id="2ef39-105">DESCRIPTION</span></span>
<span data-ttu-id="2ef39-106">Remove-AzureRmPowerBIEmbeddedCapacity Cmdlet 會刪除 PowerBI 內嵌容量的實例</span><span class="sxs-lookup"><span data-stu-id="2ef39-106">The Remove-AzureRmPowerBIEmbeddedCapacity cmdlet deletes an instance of PowerBI Embedded Capacity</span></span>

## <span data-ttu-id="2ef39-107">示例</span><span class="sxs-lookup"><span data-stu-id="2ef39-107">EXAMPLES</span></span>

### <span data-ttu-id="2ef39-108">範例1</span><span class="sxs-lookup"><span data-stu-id="2ef39-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmPowerBIEmbeddedCapacity -Name "testcapacity" -ResourceGroupName "testRG"
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

<span data-ttu-id="2ef39-109">這個命令會在 resourcegroup testRG 中移除名為 testcapacity 的容量。</span><span class="sxs-lookup"><span data-stu-id="2ef39-109">This command will remove the capacity named testcapacity in the resourcegroup testRG</span></span>

## <span data-ttu-id="2ef39-110">參數</span><span class="sxs-lookup"><span data-stu-id="2ef39-110">PARAMETERS</span></span>

### <span data-ttu-id="2ef39-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2ef39-111">-ResourceGroupName</span></span>
<span data-ttu-id="2ef39-112">容量所屬之 Azure 資源群組的名稱</span><span class="sxs-lookup"><span data-stu-id="2ef39-112">Name of the Azure resource group to which the capacity belongs</span></span>

```yaml
Type: String
Parameter Sets: ByNameAndResourceGroup
Aliases: 

Required: False
Default value: None
Accept wildcard characters: False
```

### <span data-ttu-id="2ef39-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="2ef39-113">-Name</span></span>
<span data-ttu-id="2ef39-114">PowerBI 內嵌容量的名稱</span><span class="sxs-lookup"><span data-stu-id="2ef39-114">Name of the PowerBI Embedded Capacity</span></span>

```yaml
Type: String
Parameter Sets: ByNameAndResourceGroup
Aliases: 

Required: False
Default value: None
Accept wildcard characters: False
```

### <span data-ttu-id="2ef39-115">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2ef39-115">-ResourceId</span></span>
<span data-ttu-id="2ef39-116">Azure 資源識別碼</span><span class="sxs-lookup"><span data-stu-id="2ef39-116">Azure resource ID</span></span>

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

### <span data-ttu-id="2ef39-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2ef39-117">-InputObject</span></span>
<span data-ttu-id="2ef39-118">管道的輸入物件</span><span class="sxs-lookup"><span data-stu-id="2ef39-118">Input object for Piping</span></span>

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

### <span data-ttu-id="2ef39-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2ef39-119">-PassThru</span></span>
<span data-ttu-id="2ef39-120">如果操作順利完成，將會傳回刪除的容量詳細資料</span><span class="sxs-lookup"><span data-stu-id="2ef39-120">Will return the deleted capacity details if the operation completes successfully</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ef39-121">-確認</span><span class="sxs-lookup"><span data-stu-id="2ef39-121">-Confirm</span></span>
<span data-ttu-id="2ef39-122">提示使用者確認是否要執行該作業</span><span class="sxs-lookup"><span data-stu-id="2ef39-122">Prompts user to confirm whether to perform the operation</span></span>

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

### <span data-ttu-id="2ef39-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2ef39-123">-WhatIf</span></span>
<span data-ttu-id="2ef39-124">描述目前操作將執行但不會實際執行的動作</span><span class="sxs-lookup"><span data-stu-id="2ef39-124">Describes the actions the current operation will perform without actually performing them</span></span>

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

### <span data-ttu-id="2ef39-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ef39-125">CommonParameters</span></span>
<span data-ttu-id="2ef39-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="2ef39-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ef39-127">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="2ef39-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ef39-128">輸入</span><span class="sxs-lookup"><span data-stu-id="2ef39-128">INPUTS</span></span>

### <span data-ttu-id="2ef39-129">所有</span><span class="sxs-lookup"><span data-stu-id="2ef39-129">None</span></span>
<span data-ttu-id="2ef39-130">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="2ef39-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="2ef39-131">輸出</span><span class="sxs-lookup"><span data-stu-id="2ef39-131">OUTPUTS</span></span>

### <span data-ttu-id="2ef39-132">[PSPowerBIEmbeddedCapacity] 命令。</span><span class="sxs-lookup"><span data-stu-id="2ef39-132">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="2ef39-133">筆記</span><span class="sxs-lookup"><span data-stu-id="2ef39-133">NOTES</span></span>

## <span data-ttu-id="2ef39-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="2ef39-134">RELATED LINKS</span></span>

[<span data-ttu-id="2ef39-135">AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="2ef39-135">Get-AzureRmPowerBIEmbeddedCapacity</span></span>](./Get-AzureRmPowerBIEmbeddedCapacity.md)

[<span data-ttu-id="2ef39-136">新-AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="2ef39-136">New-AzureRmPowerBIEmbeddedCapacity</span></span>](./New-AzureRmPowerBIEmbeddedCapacity.md)
