---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PowerBI.dll-Help.xml
Module Name: Az.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/powershell/module/az.powerbiembedded/update-azpowerbiembeddedcapacity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Update-AzPowerBIEmbeddedCapacity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Update-AzPowerBIEmbeddedCapacity.md
ms.openlocfilehash: 9559eb6ea0b1df4dbb25524a3a2abadffe6f6c7b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101913770"
---
# <span data-ttu-id="fab10-101">Update-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="fab10-101">Update-AzPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="fab10-102">簡介</span><span class="sxs-lookup"><span data-stu-id="fab10-102">SYNOPSIS</span></span>
<span data-ttu-id="fab10-103">修改 PowerBI 內嵌容量的實例。</span><span class="sxs-lookup"><span data-stu-id="fab10-103">Modifies  an instance of PowerBI Embedded Capacity.</span></span>

## <span data-ttu-id="fab10-104">語法</span><span class="sxs-lookup"><span data-stu-id="fab10-104">SYNTAX</span></span>

### <span data-ttu-id="fab10-105">ByNameAndResourceGroup (預設) </span><span class="sxs-lookup"><span data-stu-id="fab10-105">ByNameAndResourceGroup (Default)</span></span>
```
Update-AzPowerBIEmbeddedCapacity [-Name] <String> [-ResourceGroupName <String>] [-Sku <String>]
 [-Tag <Hashtable>] [-Administrator <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fab10-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="fab10-106">ByResourceId</span></span>
```
Update-AzPowerBIEmbeddedCapacity [-Sku <String>] [-Tag <Hashtable>] [-Administrator <String[]>]
 [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fab10-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="fab10-107">ByInputObject</span></span>
```
Update-AzPowerBIEmbeddedCapacity [-Sku <String>] [-Tag <Hashtable>] [-Administrator <String[]>]
 [-InputObject] <PSPowerBIEmbeddedCapacity> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fab10-108">描述</span><span class="sxs-lookup"><span data-stu-id="fab10-108">DESCRIPTION</span></span>
<span data-ttu-id="fab10-109">此Update-AzPowerBIEmbeddedCapacity Cmdlet 會修改 PowerBI 內嵌容量的實例</span><span class="sxs-lookup"><span data-stu-id="fab10-109">The Update-AzPowerBIEmbeddedCapacity cmdlet modifies an instance of PowerBI Embedded Capacity</span></span>

## <span data-ttu-id="fab10-110">例子</span><span class="sxs-lookup"><span data-stu-id="fab10-110">EXAMPLES</span></span>

### <span data-ttu-id="fab10-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="fab10-111">Example 1</span></span>
```
PS C:\> Update-AzPowerBIEmbeddedCapacity -Name "testcapacity" -Tag @{"key1" = "value1";"key2" = "value2"} -Administrator "testuser1@contoso.com", "testuser2@contoso.com", "9035a021-a96f-43ea-acbf-864227c2abbb@45119f4f-c71b-4420-b6ec-60e503450098" -PassThru
Type                   : Microsoft.PowerBIDedicated/capacities
Id                     : /subscriptions/78e47976-.../resourceGroups/testRG/providers/Microsoft.PowerBIDedicated/capacities/testcapacity
ResourceGroup          : testRG
Name                   : testcapacity
Location               : West Central US
State                  : Succeeded
Administrator          : {testuser1@contoso.com, testuser2@contoso.com, 9035a021-a96f-43ea-acbf-864227c2abbb@45119f4f-c71b-4420-b6ec-60e503450098}
Sku                    : A1
Tier                   : PBIE_Azure
Tag                    : {[key1, value1], [key2, value2]}
```

<span data-ttu-id="fab10-112">修改 resourcegroup testgroup 中名為 test一的容量，將標記設為 key1：value1 和 key2：value2 與系統管理員，以及 testuser1@contoso.com testuser2@contoso.com 服務主體： 9035a021-a96f-43ea-acbf-864227c2abbb@45119f4f-c71b-4420-b6ec-60e503450098</span><span class="sxs-lookup"><span data-stu-id="fab10-112">Modifies the capacity named testcapacity in resourcegroup testgroup to set the tags as key1:value1 and key2:value2 and administrator to testuser1@contoso.com , testuser2@contoso.com and the service principal: 9035a021-a96f-43ea-acbf-864227c2abbb@45119f4f-c71b-4420-b6ec-60e503450098</span></span>

## <span data-ttu-id="fab10-113">參數</span><span class="sxs-lookup"><span data-stu-id="fab10-113">PARAMETERS</span></span>

### <span data-ttu-id="fab10-114">-系統管理員</span><span class="sxs-lookup"><span data-stu-id="fab10-114">-Administrator</span></span>
<span data-ttu-id="fab10-115">在容量上設定為系統管理員的逗號分隔名稱。</span><span class="sxs-lookup"><span data-stu-id="fab10-115">A comma separated names to set as administrators on the capacity.</span></span> <span data-ttu-id="fab10-116">針對服務主體： <service principal object id>@<tenant id></span><span class="sxs-lookup"><span data-stu-id="fab10-116">For service principal: <service principal object id>@<tenant id></span></span>

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

### <span data-ttu-id="fab10-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fab10-117">-DefaultProfile</span></span>
<span data-ttu-id="fab10-118">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="fab10-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fab10-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fab10-119">-InputObject</span></span>
<span data-ttu-id="fab10-120">用於管線的輸入物件</span><span class="sxs-lookup"><span data-stu-id="fab10-120">Input object for Piping</span></span>

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

### <span data-ttu-id="fab10-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="fab10-121">-Name</span></span>
<span data-ttu-id="fab10-122">PowerBI 內嵌容量的名稱</span><span class="sxs-lookup"><span data-stu-id="fab10-122">Name of the PowerBI Embedded Capacity</span></span>

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

### <span data-ttu-id="fab10-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fab10-123">-PassThru</span></span>
<span data-ttu-id="fab10-124">如果作業順利完成，會返回已刪除的產能詳細資料</span><span class="sxs-lookup"><span data-stu-id="fab10-124">Will return the deleted capacity details if the operation completes successfully</span></span>

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

### <span data-ttu-id="fab10-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fab10-125">-ResourceGroupName</span></span>
<span data-ttu-id="fab10-126">容量所屬的 Azure 資源組名</span><span class="sxs-lookup"><span data-stu-id="fab10-126">Name of the Azure resource group to which the capacity belongs</span></span>

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

### <span data-ttu-id="fab10-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fab10-127">-ResourceId</span></span>
<span data-ttu-id="fab10-128">PowerBI 內嵌容量資源ID。</span><span class="sxs-lookup"><span data-stu-id="fab10-128">PowerBI Embedded Capacity ResourceID.</span></span>

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

### <span data-ttu-id="fab10-129">-SKU</span><span class="sxs-lookup"><span data-stu-id="fab10-129">-Sku</span></span>
<span data-ttu-id="fab10-130">容量的 SKU 名稱。</span><span class="sxs-lookup"><span data-stu-id="fab10-130">The name of the Sku for the capacity.</span></span>

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

### <span data-ttu-id="fab10-131">-標記</span><span class="sxs-lookup"><span data-stu-id="fab10-131">-Tag</span></span>
<span data-ttu-id="fab10-132">以雜湊表格形式將索引鍵值組設為容量上的標記。</span><span class="sxs-lookup"><span data-stu-id="fab10-132">Key-value pairs in the form of a hash table set as tags on the capacity.</span></span>

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

### <span data-ttu-id="fab10-133">-確認</span><span class="sxs-lookup"><span data-stu-id="fab10-133">-Confirm</span></span>
<span data-ttu-id="fab10-134">提示使用者確認是否要執行作業</span><span class="sxs-lookup"><span data-stu-id="fab10-134">Prompts user to confirm whether to perform the operation</span></span>

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

### <span data-ttu-id="fab10-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fab10-135">-WhatIf</span></span>
<span data-ttu-id="fab10-136">說明目前作業不會實際執行的動作</span><span class="sxs-lookup"><span data-stu-id="fab10-136">Describes the actions the current operation will perform without actually performing them</span></span>

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

### <span data-ttu-id="fab10-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fab10-137">CommonParameters</span></span>
<span data-ttu-id="fab10-138">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="fab10-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fab10-139">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="fab10-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fab10-140">輸入</span><span class="sxs-lookup"><span data-stu-id="fab10-140">INPUTS</span></span>

### <span data-ttu-id="fab10-141">System.String</span><span class="sxs-lookup"><span data-stu-id="fab10-141">System.String</span></span>

### <span data-ttu-id="fab10-142">Microsoft.Azure.Commands.PowerBI.models.PSPowerBIEmbeddedSoft</span><span class="sxs-lookup"><span data-stu-id="fab10-142">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="fab10-143">輸出</span><span class="sxs-lookup"><span data-stu-id="fab10-143">OUTPUTS</span></span>

### <span data-ttu-id="fab10-144">Microsoft.Azure.Commands.PowerBI.models.PSPowerBIEmbeddedSoft</span><span class="sxs-lookup"><span data-stu-id="fab10-144">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="fab10-145">筆記</span><span class="sxs-lookup"><span data-stu-id="fab10-145">NOTES</span></span>

## <span data-ttu-id="fab10-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="fab10-146">RELATED LINKS</span></span>

[<span data-ttu-id="fab10-147">Get-AzPowerBIEmbedded一切</span><span class="sxs-lookup"><span data-stu-id="fab10-147">Get-AzPowerBIEmbeddedCapacity</span></span>](./Get-AzPowerBIEmbeddedCapacity.md)

[<span data-ttu-id="fab10-148">Remove-AzPowerBIEmbedded一切</span><span class="sxs-lookup"><span data-stu-id="fab10-148">Remove-AzPowerBIEmbeddedCapacity</span></span>](./Remove-AzPowerBIEmbeddedCapacity.md)
