---
external help file: Microsoft.Azure.Commands.PowerBI.dll-Help.xml
Module Name: AzureRM.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.powerbiembedded/update-azurermpowerbiembeddedcapacity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.PowerBI/help/Update-AzureRmPowerBIEmbeddedCapacity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.PowerBI/help/Update-AzureRmPowerBIEmbeddedCapacity.md
ms.openlocfilehash: 6236a03b22bd3509933d58579db3e84d48723b68
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93455111"
---
# <span data-ttu-id="03687-101">Update-AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="03687-101">Update-AzureRmPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="03687-102">摘要</span><span class="sxs-lookup"><span data-stu-id="03687-102">SYNOPSIS</span></span>
<span data-ttu-id="03687-103">修改 PowerBI 內嵌容量的實例。</span><span class="sxs-lookup"><span data-stu-id="03687-103">Modifies  an instance of PowerBI Embedded Capacity.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="03687-104">句法</span><span class="sxs-lookup"><span data-stu-id="03687-104">SYNTAX</span></span>

### <span data-ttu-id="03687-105">ByNameAndResourceGroup (預設) </span><span class="sxs-lookup"><span data-stu-id="03687-105">ByNameAndResourceGroup (Default)</span></span>
```
Update-AzureRmPowerBIEmbeddedCapacity [-Name] <String> [-ResourceGroupName <String>] [-Sku <String>]
 [-Tag <Hashtable>] [-Administrator <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="03687-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="03687-106">ByResourceId</span></span>
```
Update-AzureRmPowerBIEmbeddedCapacity [-Sku <String>] [-Tag <Hashtable>] [-Administrator <String[]>]
 [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="03687-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="03687-107">ByInputObject</span></span>
```
Update-AzureRmPowerBIEmbeddedCapacity [-Sku <String>] [-Tag <Hashtable>] [-Administrator <String[]>]
 [-InputObject] <PSPowerBIEmbeddedCapacity> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="03687-108">說明</span><span class="sxs-lookup"><span data-stu-id="03687-108">DESCRIPTION</span></span>
<span data-ttu-id="03687-109">Update-AzureRmPowerBIEmbeddedCapacity Cmdlet 會修改 PowerBI 內嵌容量的實例</span><span class="sxs-lookup"><span data-stu-id="03687-109">The Update-AzureRmPowerBIEmbeddedCapacity cmdlet modifies an instance of PowerBI Embedded Capacity</span></span>

## <span data-ttu-id="03687-110">示例</span><span class="sxs-lookup"><span data-stu-id="03687-110">EXAMPLES</span></span>

### <span data-ttu-id="03687-111">範例1</span><span class="sxs-lookup"><span data-stu-id="03687-111">Example 1</span></span>
```
PS C:\> Update-AzureRmPowerBIEmbeddedCapacity -Name "testcapacity" -Tag @{"key1" = "value1";"key2" = "value2"} -Administrator "testuser1@contoso.com, testuser2@contoso.com" -PassThru
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

<span data-ttu-id="03687-112">修改 resourcegroup testgroup 中名為 testcapacity 的容量，將標籤設為 key1： value1 和 key2： value2 與 administrator testuser1@contoso.com</span><span class="sxs-lookup"><span data-stu-id="03687-112">Modifies the capacity named testcapacity in resourcegroup testgroup to set the tags as key1:value1 and key2:value2 and administrator to testuser1@contoso.com</span></span>

## <span data-ttu-id="03687-113">參數</span><span class="sxs-lookup"><span data-stu-id="03687-113">PARAMETERS</span></span>

### <span data-ttu-id="03687-114">-系統管理員</span><span class="sxs-lookup"><span data-stu-id="03687-114">-Administrator</span></span>
<span data-ttu-id="03687-115">以逗號分隔的容量名稱，在容量上設定為系統管理員</span><span class="sxs-lookup"><span data-stu-id="03687-115">A comma separated capacity names to set as administrator on the capacity</span></span>

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

### <span data-ttu-id="03687-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03687-116">-DefaultProfile</span></span>
<span data-ttu-id="03687-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="03687-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="03687-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="03687-118">-InputObject</span></span>
<span data-ttu-id="03687-119">管道的輸入物件</span><span class="sxs-lookup"><span data-stu-id="03687-119">Input object for Piping</span></span>

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

### <span data-ttu-id="03687-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="03687-120">-Name</span></span>
<span data-ttu-id="03687-121">PowerBI 內嵌容量的名稱</span><span class="sxs-lookup"><span data-stu-id="03687-121">Name of the PowerBI Embedded Capacity</span></span>

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

### <span data-ttu-id="03687-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="03687-122">-PassThru</span></span>
<span data-ttu-id="03687-123">如果操作順利完成，將會傳回刪除的容量詳細資料</span><span class="sxs-lookup"><span data-stu-id="03687-123">Will return the deleted capacity details if the operation completes successfully</span></span>

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

### <span data-ttu-id="03687-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="03687-124">-ResourceGroupName</span></span>
<span data-ttu-id="03687-125">容量所屬之 Azure 資源群組的名稱</span><span class="sxs-lookup"><span data-stu-id="03687-125">Name of the Azure resource group to which the capacity belongs</span></span>

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

### <span data-ttu-id="03687-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="03687-126">-ResourceId</span></span>
<span data-ttu-id="03687-127">PowerBI 內嵌容量 ResourceID。</span><span class="sxs-lookup"><span data-stu-id="03687-127">PowerBI Embedded Capacity ResourceID.</span></span>

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

### <span data-ttu-id="03687-128">-Sku</span><span class="sxs-lookup"><span data-stu-id="03687-128">-Sku</span></span>
<span data-ttu-id="03687-129">容量的 Sku 名稱。</span><span class="sxs-lookup"><span data-stu-id="03687-129">The name of the Sku for the capacity.</span></span>

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

### <span data-ttu-id="03687-130">-Tag</span><span class="sxs-lookup"><span data-stu-id="03687-130">-Tag</span></span>
<span data-ttu-id="03687-131">雜湊資料表形式的鍵值對，在容量中設為標記。</span><span class="sxs-lookup"><span data-stu-id="03687-131">Key-value pairs in the form of a hash table set as tags on the capacity.</span></span>

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

### <span data-ttu-id="03687-132">-確認</span><span class="sxs-lookup"><span data-stu-id="03687-132">-Confirm</span></span>
<span data-ttu-id="03687-133">提示使用者確認是否要執行該作業</span><span class="sxs-lookup"><span data-stu-id="03687-133">Prompts user to confirm whether to perform the operation</span></span>

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

### <span data-ttu-id="03687-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="03687-134">-WhatIf</span></span>
<span data-ttu-id="03687-135">描述目前操作將執行但不會實際執行的動作</span><span class="sxs-lookup"><span data-stu-id="03687-135">Describes the actions the current operation will perform without actually performing them</span></span>

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

### <span data-ttu-id="03687-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03687-136">CommonParameters</span></span>
<span data-ttu-id="03687-137">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="03687-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03687-138">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="03687-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03687-139">輸入</span><span class="sxs-lookup"><span data-stu-id="03687-139">INPUTS</span></span>

### <span data-ttu-id="03687-140">System.object</span><span class="sxs-lookup"><span data-stu-id="03687-140">System.String</span></span>

### <span data-ttu-id="03687-141">[PSPowerBIEmbeddedCapacity] 命令。</span><span class="sxs-lookup"><span data-stu-id="03687-141">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>
<span data-ttu-id="03687-142">參數： InputObject (ByValue) </span><span class="sxs-lookup"><span data-stu-id="03687-142">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="03687-143">輸出</span><span class="sxs-lookup"><span data-stu-id="03687-143">OUTPUTS</span></span>

### <span data-ttu-id="03687-144">[PSPowerBIEmbeddedCapacity] 命令。</span><span class="sxs-lookup"><span data-stu-id="03687-144">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="03687-145">筆記</span><span class="sxs-lookup"><span data-stu-id="03687-145">NOTES</span></span>

## <span data-ttu-id="03687-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="03687-146">RELATED LINKS</span></span>

[<span data-ttu-id="03687-147">AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="03687-147">Get-AzureRmPowerBIEmbeddedCapacity</span></span>](./Get-AzureRmPowerBIEmbeddedCapacity.md)

[<span data-ttu-id="03687-148">移除-AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="03687-148">Remove-AzureRmPowerBIEmbeddedCapacity</span></span>](./Remove-AzureRmPowerBIEmbeddedCapacity.md)
