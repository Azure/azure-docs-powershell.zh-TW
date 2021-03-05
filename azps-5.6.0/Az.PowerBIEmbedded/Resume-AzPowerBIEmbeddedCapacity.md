---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PowerBI.dll-Help.xml
Module Name: Az.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/powershell/module/az.powerbiembedded/resume-azpowerbiembeddedcapacity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Resume-AzPowerBIEmbeddedCapacity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Resume-AzPowerBIEmbeddedCapacity.md
ms.openlocfilehash: cd0eab8d5670f8c37d45c8e0e211100749aa7a4d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101917962"
---
# <span data-ttu-id="84ecf-101">Resume-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="84ecf-101">Resume-AzPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="84ecf-102">簡介</span><span class="sxs-lookup"><span data-stu-id="84ecf-102">SYNOPSIS</span></span>
<span data-ttu-id="84ecf-103">繼續 PowerBI 內嵌容量的實例。</span><span class="sxs-lookup"><span data-stu-id="84ecf-103">Resumes an instance of PowerBI Embedded Capacity.</span></span>

## <span data-ttu-id="84ecf-104">語法</span><span class="sxs-lookup"><span data-stu-id="84ecf-104">SYNTAX</span></span>

### <span data-ttu-id="84ecf-105">ByNameAndResourceGroup (預設) </span><span class="sxs-lookup"><span data-stu-id="84ecf-105">ByNameAndResourceGroup (Default)</span></span>
```
Resume-AzPowerBIEmbeddedCapacity [-Name] <String> [-ResourceGroupName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="84ecf-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="84ecf-106">ByResourceId</span></span>
```
Resume-AzPowerBIEmbeddedCapacity [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="84ecf-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="84ecf-107">ByInputObject</span></span>
```
Resume-AzPowerBIEmbeddedCapacity [-InputObject] <PSPowerBIEmbeddedCapacity> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="84ecf-108">描述</span><span class="sxs-lookup"><span data-stu-id="84ecf-108">DESCRIPTION</span></span>
<span data-ttu-id="84ecf-109">此Resume-AzPowerBIEmbeddedCapacity Cmdlet 會繼續 PowerBI 內嵌容量的實例</span><span class="sxs-lookup"><span data-stu-id="84ecf-109">The Resume-AzPowerBIEmbeddedCapacity cmdlet resumes an instance of PowerBI Embedded Capacity</span></span>

## <span data-ttu-id="84ecf-110">例子</span><span class="sxs-lookup"><span data-stu-id="84ecf-110">EXAMPLES</span></span>

### <span data-ttu-id="84ecf-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="84ecf-111">Example 1</span></span>
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

<span data-ttu-id="84ecf-112">此命令會繼續資源組 testRG 中名為 test一的已暫停容量</span><span class="sxs-lookup"><span data-stu-id="84ecf-112">This command will resume a paused capacity named testcapacity in the resourcegroup testRG</span></span>

## <span data-ttu-id="84ecf-113">參數</span><span class="sxs-lookup"><span data-stu-id="84ecf-113">PARAMETERS</span></span>

### <span data-ttu-id="84ecf-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84ecf-114">-DefaultProfile</span></span>
<span data-ttu-id="84ecf-115">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="84ecf-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="84ecf-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="84ecf-116">-InputObject</span></span>
<span data-ttu-id="84ecf-117">用於管線的輸入物件</span><span class="sxs-lookup"><span data-stu-id="84ecf-117">Input object for Piping</span></span>

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

### <span data-ttu-id="84ecf-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="84ecf-118">-Name</span></span>
<span data-ttu-id="84ecf-119">PowerBI 內嵌容量的名稱</span><span class="sxs-lookup"><span data-stu-id="84ecf-119">Name of the PowerBI Embedded Capacity</span></span>

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

### <span data-ttu-id="84ecf-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="84ecf-120">-PassThru</span></span>
<span data-ttu-id="84ecf-121">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="84ecf-121">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="84ecf-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="84ecf-122">-ResourceGroupName</span></span>
<span data-ttu-id="84ecf-123">容量所屬的 Azure 資源組名</span><span class="sxs-lookup"><span data-stu-id="84ecf-123">Name of the Azure resource group to which the capacity belongs</span></span>

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

### <span data-ttu-id="84ecf-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="84ecf-124">-ResourceId</span></span>
<span data-ttu-id="84ecf-125">Azure 資源識別碼</span><span class="sxs-lookup"><span data-stu-id="84ecf-125">Azure resource ID</span></span>

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

### <span data-ttu-id="84ecf-126">-確認</span><span class="sxs-lookup"><span data-stu-id="84ecf-126">-Confirm</span></span>
<span data-ttu-id="84ecf-127">提示使用者確認是否要執行作業</span><span class="sxs-lookup"><span data-stu-id="84ecf-127">Prompts user to confirm whether to perform the operation</span></span>

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

### <span data-ttu-id="84ecf-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="84ecf-128">-WhatIf</span></span>
<span data-ttu-id="84ecf-129">說明目前作業不會實際執行的動作</span><span class="sxs-lookup"><span data-stu-id="84ecf-129">Describes the actions the current operation will perform without actually performing them</span></span>

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

### <span data-ttu-id="84ecf-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84ecf-130">CommonParameters</span></span>
<span data-ttu-id="84ecf-131">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="84ecf-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84ecf-132">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="84ecf-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84ecf-133">輸入</span><span class="sxs-lookup"><span data-stu-id="84ecf-133">INPUTS</span></span>

### <span data-ttu-id="84ecf-134">System.String</span><span class="sxs-lookup"><span data-stu-id="84ecf-134">System.String</span></span>

### <span data-ttu-id="84ecf-135">Microsoft.Azure.Commands.PowerBI.models.PSPowerBIEmbeddedSoft</span><span class="sxs-lookup"><span data-stu-id="84ecf-135">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="84ecf-136">輸出</span><span class="sxs-lookup"><span data-stu-id="84ecf-136">OUTPUTS</span></span>

### <span data-ttu-id="84ecf-137">Microsoft.Azure.Commands.PowerBI.models.PSPowerBIEmbeddedSoft</span><span class="sxs-lookup"><span data-stu-id="84ecf-137">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="84ecf-138">筆記</span><span class="sxs-lookup"><span data-stu-id="84ecf-138">NOTES</span></span>

## <span data-ttu-id="84ecf-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="84ecf-139">RELATED LINKS</span></span>

[<span data-ttu-id="84ecf-140">Get-AzPowerBIEmbedded一切</span><span class="sxs-lookup"><span data-stu-id="84ecf-140">Get-AzPowerBIEmbeddedCapacity</span></span>](./Get-AzPowerBIEmbeddedCapacity.md)

[<span data-ttu-id="84ecf-141">Suspend-AzPowerBIEmbedded一切</span><span class="sxs-lookup"><span data-stu-id="84ecf-141">Suspend-AzPowerBIEmbeddedCapacity</span></span>](./Suspend-AzPowerBIEmbeddedCapacity.md)
