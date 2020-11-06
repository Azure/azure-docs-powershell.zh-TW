---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PowerBI.dll-Help.xml
Module Name: Az.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/en-us/powershell/module/az.powerbiembedded/update-azpowerbiembeddedcapacity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Update-AzPowerBIEmbeddedCapacity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Update-AzPowerBIEmbeddedCapacity.md
ms.openlocfilehash: bed116bedbd06919728da8727cad609813bfc2a0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93621234"
---
# <span data-ttu-id="bc4dc-101">Update-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="bc4dc-101">Update-AzPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="bc4dc-102">摘要</span><span class="sxs-lookup"><span data-stu-id="bc4dc-102">SYNOPSIS</span></span>
<span data-ttu-id="bc4dc-103">修改 PowerBI 內嵌容量的實例。</span><span class="sxs-lookup"><span data-stu-id="bc4dc-103">Modifies  an instance of PowerBI Embedded Capacity.</span></span>

## <span data-ttu-id="bc4dc-104">句法</span><span class="sxs-lookup"><span data-stu-id="bc4dc-104">SYNTAX</span></span>

### <span data-ttu-id="bc4dc-105">ByNameAndResourceGroup (預設) </span><span class="sxs-lookup"><span data-stu-id="bc4dc-105">ByNameAndResourceGroup (Default)</span></span>
```
Update-AzPowerBIEmbeddedCapacity [-Name] <String> [-ResourceGroupName <String>] [-Sku <String>]
 [-Tag <Hashtable>] [-Administrator <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bc4dc-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="bc4dc-106">ByResourceId</span></span>
```
Update-AzPowerBIEmbeddedCapacity [-Sku <String>] [-Tag <Hashtable>] [-Administrator <String[]>]
 [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="bc4dc-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="bc4dc-107">ByInputObject</span></span>
```
Update-AzPowerBIEmbeddedCapacity [-Sku <String>] [-Tag <Hashtable>] [-Administrator <String[]>]
 [-InputObject] <PSPowerBIEmbeddedCapacity> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bc4dc-108">說明</span><span class="sxs-lookup"><span data-stu-id="bc4dc-108">DESCRIPTION</span></span>
<span data-ttu-id="bc4dc-109">Update-AzPowerBIEmbeddedCapacity Cmdlet 會修改 PowerBI 內嵌容量的實例</span><span class="sxs-lookup"><span data-stu-id="bc4dc-109">The Update-AzPowerBIEmbeddedCapacity cmdlet modifies an instance of PowerBI Embedded Capacity</span></span>

## <span data-ttu-id="bc4dc-110">示例</span><span class="sxs-lookup"><span data-stu-id="bc4dc-110">EXAMPLES</span></span>

### <span data-ttu-id="bc4dc-111">範例1</span><span class="sxs-lookup"><span data-stu-id="bc4dc-111">Example 1</span></span>
```
PS C:\> Update-AzPowerBIEmbeddedCapacity -Name "testcapacity" -Tag @{"key1" = "value1";"key2" = "value2"} -Administrator "testuser1@contoso.com, testuser2@contoso.com" -PassThru
Type                   : Microsoft.PowerBIDedicated/capacities
Id                     : /subscriptions/78e47976-.../resourceGroups/testRG/providers/Microsoft.PowerBIDedicated/capacities/testcapacity
ResourceGroup          : testRG
Name                   : testcapacity
Location               : West Central US
State                  : Succeeded
Administrator          : {testuser1@contoso.com, testuser2@contoso.com}
Sku                    : A1
Tier                   : PBIE_Azure
Tag                    : {[key1, value1], [key2, value2]}
```

<span data-ttu-id="bc4dc-112">修改 resourcegroup testgroup 中名為 testcapacity 的容量，將標籤設為 key1： value1 和 key2： value2 與 administrator testuser1@contoso.com</span><span class="sxs-lookup"><span data-stu-id="bc4dc-112">Modifies the capacity named testcapacity in resourcegroup testgroup to set the tags as key1:value1 and key2:value2 and administrator to testuser1@contoso.com</span></span>

## <span data-ttu-id="bc4dc-113">參數</span><span class="sxs-lookup"><span data-stu-id="bc4dc-113">PARAMETERS</span></span>

### <span data-ttu-id="bc4dc-114">-系統管理員</span><span class="sxs-lookup"><span data-stu-id="bc4dc-114">-Administrator</span></span>
<span data-ttu-id="bc4dc-115">以逗號分隔的容量名稱，在容量上設定為系統管理員</span><span class="sxs-lookup"><span data-stu-id="bc4dc-115">A comma separated capacity names to set as administrator on the capacity</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc4dc-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bc4dc-116">-DefaultProfile</span></span>
<span data-ttu-id="bc4dc-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="bc4dc-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bc4dc-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bc4dc-118">-InputObject</span></span>
<span data-ttu-id="bc4dc-119">管道的輸入物件</span><span class="sxs-lookup"><span data-stu-id="bc4dc-119">Input object for Piping</span></span>

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

### <span data-ttu-id="bc4dc-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="bc4dc-120">-Name</span></span>
<span data-ttu-id="bc4dc-121">PowerBI 內嵌容量的名稱</span><span class="sxs-lookup"><span data-stu-id="bc4dc-121">Name of the PowerBI Embedded Capacity</span></span>

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

### <span data-ttu-id="bc4dc-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bc4dc-122">-PassThru</span></span>
<span data-ttu-id="bc4dc-123">如果操作順利完成，將會傳回刪除的容量詳細資料</span><span class="sxs-lookup"><span data-stu-id="bc4dc-123">Will return the deleted capacity details if the operation completes successfully</span></span>

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

### <span data-ttu-id="bc4dc-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bc4dc-124">-ResourceGroupName</span></span>
<span data-ttu-id="bc4dc-125">容量所屬之 Azure 資源群組的名稱</span><span class="sxs-lookup"><span data-stu-id="bc4dc-125">Name of the Azure resource group to which the capacity belongs</span></span>

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

### <span data-ttu-id="bc4dc-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bc4dc-126">-ResourceId</span></span>
<span data-ttu-id="bc4dc-127">PowerBI 內嵌容量 ResourceID。</span><span class="sxs-lookup"><span data-stu-id="bc4dc-127">PowerBI Embedded Capacity ResourceID.</span></span>

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

### <span data-ttu-id="bc4dc-128">-Sku</span><span class="sxs-lookup"><span data-stu-id="bc4dc-128">-Sku</span></span>
<span data-ttu-id="bc4dc-129">容量的 Sku 名稱。</span><span class="sxs-lookup"><span data-stu-id="bc4dc-129">The name of the Sku for the capacity.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: A1, A2, A3, A4, A5, A6

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc4dc-130">-Tag</span><span class="sxs-lookup"><span data-stu-id="bc4dc-130">-Tag</span></span>
<span data-ttu-id="bc4dc-131">雜湊資料表形式的鍵值對，在容量中設為標記。</span><span class="sxs-lookup"><span data-stu-id="bc4dc-131">Key-value pairs in the form of a hash table set as tags on the capacity.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc4dc-132">-確認</span><span class="sxs-lookup"><span data-stu-id="bc4dc-132">-Confirm</span></span>
<span data-ttu-id="bc4dc-133">提示使用者確認是否要執行該作業</span><span class="sxs-lookup"><span data-stu-id="bc4dc-133">Prompts user to confirm whether to perform the operation</span></span>

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

### <span data-ttu-id="bc4dc-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bc4dc-134">-WhatIf</span></span>
<span data-ttu-id="bc4dc-135">描述目前操作將執行但不會實際執行的動作</span><span class="sxs-lookup"><span data-stu-id="bc4dc-135">Describes the actions the current operation will perform without actually performing them</span></span>

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

### <span data-ttu-id="bc4dc-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc4dc-136">CommonParameters</span></span>
<span data-ttu-id="bc4dc-137">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="bc4dc-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc4dc-138">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="bc4dc-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc4dc-139">輸入</span><span class="sxs-lookup"><span data-stu-id="bc4dc-139">INPUTS</span></span>

### <span data-ttu-id="bc4dc-140">System.object</span><span class="sxs-lookup"><span data-stu-id="bc4dc-140">System.String</span></span>

### <span data-ttu-id="bc4dc-141">[PSPowerBIEmbeddedCapacity] 命令。</span><span class="sxs-lookup"><span data-stu-id="bc4dc-141">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="bc4dc-142">輸出</span><span class="sxs-lookup"><span data-stu-id="bc4dc-142">OUTPUTS</span></span>

### <span data-ttu-id="bc4dc-143">[PSPowerBIEmbeddedCapacity] 命令。</span><span class="sxs-lookup"><span data-stu-id="bc4dc-143">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="bc4dc-144">筆記</span><span class="sxs-lookup"><span data-stu-id="bc4dc-144">NOTES</span></span>

## <span data-ttu-id="bc4dc-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="bc4dc-145">RELATED LINKS</span></span>

[<span data-ttu-id="bc4dc-146">AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="bc4dc-146">Get-AzPowerBIEmbeddedCapacity</span></span>](./Get-AzPowerBIEmbeddedCapacity.md)

[<span data-ttu-id="bc4dc-147">移除-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="bc4dc-147">Remove-AzPowerBIEmbeddedCapacity</span></span>](./Remove-AzPowerBIEmbeddedCapacity.md)
