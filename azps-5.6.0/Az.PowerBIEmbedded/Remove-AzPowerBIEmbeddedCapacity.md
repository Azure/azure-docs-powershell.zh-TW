---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PowerBI.dll-Help.xml
Module Name: Az.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/powershell/module/az.powerbiembedded/remove-azpowerbiembeddedcapacity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Remove-AzPowerBIEmbeddedCapacity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Remove-AzPowerBIEmbeddedCapacity.md
ms.openlocfilehash: 93c15d2675cc0e3e5fe0b37bc5af331ce97e7d8b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101902285"
---
# <span data-ttu-id="382b1-101">Remove-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="382b1-101">Remove-AzPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="382b1-102">簡介</span><span class="sxs-lookup"><span data-stu-id="382b1-102">SYNOPSIS</span></span>
<span data-ttu-id="382b1-103">刪除 PowerBI 內嵌容量的實例。</span><span class="sxs-lookup"><span data-stu-id="382b1-103">Deletes an instance of PowerBI Embedded Capacity.</span></span>

## <span data-ttu-id="382b1-104">語法</span><span class="sxs-lookup"><span data-stu-id="382b1-104">SYNTAX</span></span>

### <span data-ttu-id="382b1-105">ByNameAndResourceGroup (預設) </span><span class="sxs-lookup"><span data-stu-id="382b1-105">ByNameAndResourceGroup (Default)</span></span>
```
Remove-AzPowerBIEmbeddedCapacity [-Name] <String> [-ResourceGroupName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="382b1-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="382b1-106">ByResourceId</span></span>
```
Remove-AzPowerBIEmbeddedCapacity [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="382b1-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="382b1-107">ByInputObject</span></span>
```
Remove-AzPowerBIEmbeddedCapacity [-InputObject] <PSPowerBIEmbeddedCapacity> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="382b1-108">描述</span><span class="sxs-lookup"><span data-stu-id="382b1-108">DESCRIPTION</span></span>
<span data-ttu-id="382b1-109">此Remove-AzPowerBIEmbeddedCapacity Cmdlet 會刪除 PowerBI 內嵌容量的實例</span><span class="sxs-lookup"><span data-stu-id="382b1-109">The Remove-AzPowerBIEmbeddedCapacity cmdlet deletes an instance of PowerBI Embedded Capacity</span></span>

## <span data-ttu-id="382b1-110">例子</span><span class="sxs-lookup"><span data-stu-id="382b1-110">EXAMPLES</span></span>

### <span data-ttu-id="382b1-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="382b1-111">Example 1</span></span>
```
PS C:\> Remove-AzPowerBIEmbeddedCapacity -Name "testcapacity" -ResourceGroupName "testRG"
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

<span data-ttu-id="382b1-112">此命令會移除資源組 testRG 中名為 test一的容量</span><span class="sxs-lookup"><span data-stu-id="382b1-112">This command will remove the capacity named testcapacity in the resourcegroup testRG</span></span>

## <span data-ttu-id="382b1-113">參數</span><span class="sxs-lookup"><span data-stu-id="382b1-113">PARAMETERS</span></span>

### <span data-ttu-id="382b1-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="382b1-114">-DefaultProfile</span></span>
<span data-ttu-id="382b1-115">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="382b1-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="382b1-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="382b1-116">-InputObject</span></span>
<span data-ttu-id="382b1-117">用於管線的輸入物件</span><span class="sxs-lookup"><span data-stu-id="382b1-117">Input object for Piping</span></span>

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

### <span data-ttu-id="382b1-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="382b1-118">-Name</span></span>
<span data-ttu-id="382b1-119">PowerBI 內嵌容量的名稱</span><span class="sxs-lookup"><span data-stu-id="382b1-119">Name of the PowerBI Embedded Capacity</span></span>

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

### <span data-ttu-id="382b1-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="382b1-120">-PassThru</span></span>
<span data-ttu-id="382b1-121">如果作業順利完成，會返回已刪除的產能詳細資料</span><span class="sxs-lookup"><span data-stu-id="382b1-121">Will return the deleted capacity details if the operation completes successfully</span></span>

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

### <span data-ttu-id="382b1-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="382b1-122">-ResourceGroupName</span></span>
<span data-ttu-id="382b1-123">容量所屬的 Azure 資源組名</span><span class="sxs-lookup"><span data-stu-id="382b1-123">Name of the Azure resource group to which the capacity belongs</span></span>

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

### <span data-ttu-id="382b1-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="382b1-124">-ResourceId</span></span>
<span data-ttu-id="382b1-125">Azure 資源識別碼</span><span class="sxs-lookup"><span data-stu-id="382b1-125">Azure resource ID</span></span>

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

### <span data-ttu-id="382b1-126">-確認</span><span class="sxs-lookup"><span data-stu-id="382b1-126">-Confirm</span></span>
<span data-ttu-id="382b1-127">提示使用者確認是否要執行作業</span><span class="sxs-lookup"><span data-stu-id="382b1-127">Prompts user to confirm whether to perform the operation</span></span>

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

### <span data-ttu-id="382b1-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="382b1-128">-WhatIf</span></span>
<span data-ttu-id="382b1-129">說明目前作業不會實際執行的動作</span><span class="sxs-lookup"><span data-stu-id="382b1-129">Describes the actions the current operation will perform without actually performing them</span></span>

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

### <span data-ttu-id="382b1-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="382b1-130">CommonParameters</span></span>
<span data-ttu-id="382b1-131">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="382b1-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="382b1-132">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="382b1-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="382b1-133">輸入</span><span class="sxs-lookup"><span data-stu-id="382b1-133">INPUTS</span></span>

### <span data-ttu-id="382b1-134">System.String</span><span class="sxs-lookup"><span data-stu-id="382b1-134">System.String</span></span>

### <span data-ttu-id="382b1-135">Microsoft.Azure.Commands.PowerBI.models.PSPowerBIEmbeddedSoft</span><span class="sxs-lookup"><span data-stu-id="382b1-135">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="382b1-136">輸出</span><span class="sxs-lookup"><span data-stu-id="382b1-136">OUTPUTS</span></span>

### <span data-ttu-id="382b1-137">Microsoft.Azure.Commands.PowerBI.models.PSPowerBIEmbeddedSoft</span><span class="sxs-lookup"><span data-stu-id="382b1-137">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="382b1-138">筆記</span><span class="sxs-lookup"><span data-stu-id="382b1-138">NOTES</span></span>

## <span data-ttu-id="382b1-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="382b1-139">RELATED LINKS</span></span>

[<span data-ttu-id="382b1-140">Get-AzPowerBIEmbedded一切</span><span class="sxs-lookup"><span data-stu-id="382b1-140">Get-AzPowerBIEmbeddedCapacity</span></span>](./Get-AzPowerBIEmbeddedCapacity.md)

[<span data-ttu-id="382b1-141">New-AzPowerBIEmbedded一切</span><span class="sxs-lookup"><span data-stu-id="382b1-141">New-AzPowerBIEmbeddedCapacity</span></span>](./New-AzPowerBIEmbeddedCapacity.md)
