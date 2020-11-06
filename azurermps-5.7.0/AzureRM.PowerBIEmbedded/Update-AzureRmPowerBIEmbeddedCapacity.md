---
external help file: Microsoft.Azure.Commands.PowerBI.dll-Help.xml
Module Name: AzureRM.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.powerbiembedded/update-azurermpowerbiembeddedcapacity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.PowerBI/help/Update-AzureRmPowerBIEmbeddedCapacity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.PowerBI/help/Update-AzureRmPowerBIEmbeddedCapacity.md
ms.openlocfilehash: 64e96f423748e8991abcf26b178a8bd6b893cf0a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93444463"
---
# <span data-ttu-id="aabed-101">Update-AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="aabed-101">Update-AzureRmPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="aabed-102">摘要</span><span class="sxs-lookup"><span data-stu-id="aabed-102">SYNOPSIS</span></span>
<span data-ttu-id="aabed-103">修改 PowerBI 內嵌容量的實例。</span><span class="sxs-lookup"><span data-stu-id="aabed-103">Modifies  an instance of PowerBI Embedded Capacity.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="aabed-104">句法</span><span class="sxs-lookup"><span data-stu-id="aabed-104">SYNTAX</span></span>

```
Update-AzureRmPowerBIEmbeddedCapacity 
    [-Name] <String> 
    [[-ResourceGroupName] <String>] 
    [[-Sku] <String>]
    [[-Tag] <Hashtable>] 
    [[-Administrator] <String>] 
    [-PassThru] 
    [-WhatIf]
    [-Confirm] 
    [<CommonParameters>]
```

## <span data-ttu-id="aabed-105">說明</span><span class="sxs-lookup"><span data-stu-id="aabed-105">DESCRIPTION</span></span>
<span data-ttu-id="aabed-106">Update-AzureRmPowerBIEmbeddedCapacity Cmdlet 會修改 PowerBI 內嵌容量的實例</span><span class="sxs-lookup"><span data-stu-id="aabed-106">The Update-AzureRmPowerBIEmbeddedCapacity cmdlet modifies an instance of PowerBI Embedded Capacity</span></span>

## <span data-ttu-id="aabed-107">示例</span><span class="sxs-lookup"><span data-stu-id="aabed-107">EXAMPLES</span></span>

### <span data-ttu-id="aabed-108">範例1</span><span class="sxs-lookup"><span data-stu-id="aabed-108">Example 1</span></span>
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

<span data-ttu-id="aabed-109">修改 resourcegroup testgroup 中名為 testcapacity 的容量，將標籤設為 key1： value1 和 key2： value2 與 administrator testuser1@contoso.com</span><span class="sxs-lookup"><span data-stu-id="aabed-109">Modifies the capacity named testcapacity in resourcegroup testgroup to set the tags as key1:value1 and key2:value2 and administrator to testuser1@contoso.com</span></span>

## <span data-ttu-id="aabed-110">參數</span><span class="sxs-lookup"><span data-stu-id="aabed-110">PARAMETERS</span></span>

### <span data-ttu-id="aabed-111">-名稱</span><span class="sxs-lookup"><span data-stu-id="aabed-111">-Name</span></span>
<span data-ttu-id="aabed-112">PowerBI 內嵌容量的名稱</span><span class="sxs-lookup"><span data-stu-id="aabed-112">Name of the PowerBI Embedded Capacity</span></span>

```yaml
Type: String
Parameter Sets: ByNameAndResourceGroup
Aliases: 

Required: True
Position: 0
Default value: None
Accept wildcard characters: False
```

### <span data-ttu-id="aabed-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aabed-113">-ResourceGroupName</span></span>
<span data-ttu-id="aabed-114">容量所屬之 Azure 資源群組的名稱</span><span class="sxs-lookup"><span data-stu-id="aabed-114">Name of the Azure resource group to which the capacity belongs</span></span>

```yaml
Type: String
Parameter Sets: ByNameAndResourceGroup
Aliases: 

Required: False
Default value: None
Accept wildcard characters: False
```

### <span data-ttu-id="aabed-115">-Sku</span><span class="sxs-lookup"><span data-stu-id="aabed-115">-Sku</span></span>
<span data-ttu-id="aabed-116">容量的 Sku 名稱。</span><span class="sxs-lookup"><span data-stu-id="aabed-116">The name of the Sku for the capacity.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: A1, A2, A3, A4, A5, A6

Required: False
Default value: None
Accept wildcard characters: False
```

### <span data-ttu-id="aabed-117">-Tag</span><span class="sxs-lookup"><span data-stu-id="aabed-117">-Tag</span></span>
<span data-ttu-id="aabed-118">雜湊資料表形式的鍵值對，在容量中設為標記。</span><span class="sxs-lookup"><span data-stu-id="aabed-118">Key-value pairs in the form of a hash table set as tags on the capacity.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Default value: None
Accept wildcard characters: False
```
### <span data-ttu-id="aabed-119">-系統管理員</span><span class="sxs-lookup"><span data-stu-id="aabed-119">-Administrator</span></span>
<span data-ttu-id="aabed-120">以逗號分隔的容量名稱，在容量上設定為系統管理員</span><span class="sxs-lookup"><span data-stu-id="aabed-120">A comma separated capacity names to set as administrator on the capacity</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Default value: None
Accept wildcard characters: False
```

### <span data-ttu-id="aabed-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="aabed-121">-ResourceId</span></span>
<span data-ttu-id="aabed-122">PowerBI 內嵌容量 ResourceID。</span><span class="sxs-lookup"><span data-stu-id="aabed-122">PowerBI Embedded Capacity ResourceID.</span></span>

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

### <span data-ttu-id="aabed-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="aabed-123">-InputObject</span></span>
<span data-ttu-id="aabed-124">管道的輸入物件</span><span class="sxs-lookup"><span data-stu-id="aabed-124">Input object for Piping</span></span>

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

### <span data-ttu-id="aabed-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="aabed-125">-PassThru</span></span>
<span data-ttu-id="aabed-126">如果操作順利完成，將會傳回刪除的容量詳細資料</span><span class="sxs-lookup"><span data-stu-id="aabed-126">Will return the deleted capacity details if the operation completes successfully</span></span>

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

### <span data-ttu-id="aabed-127">-確認</span><span class="sxs-lookup"><span data-stu-id="aabed-127">-Confirm</span></span>
<span data-ttu-id="aabed-128">提示使用者確認是否要執行該作業</span><span class="sxs-lookup"><span data-stu-id="aabed-128">Prompts user to confirm whether to perform the operation</span></span>

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

### <span data-ttu-id="aabed-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aabed-129">-WhatIf</span></span>
<span data-ttu-id="aabed-130">描述目前操作將執行但不會實際執行的動作</span><span class="sxs-lookup"><span data-stu-id="aabed-130">Describes the actions the current operation will perform without actually performing them</span></span>

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

### <span data-ttu-id="aabed-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aabed-131">CommonParameters</span></span>
<span data-ttu-id="aabed-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="aabed-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aabed-133">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="aabed-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aabed-134">輸入</span><span class="sxs-lookup"><span data-stu-id="aabed-134">INPUTS</span></span>

### <span data-ttu-id="aabed-135">所有</span><span class="sxs-lookup"><span data-stu-id="aabed-135">None</span></span>
<span data-ttu-id="aabed-136">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="aabed-136">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="aabed-137">輸出</span><span class="sxs-lookup"><span data-stu-id="aabed-137">OUTPUTS</span></span>

### <span data-ttu-id="aabed-138">[PSPowerBIEmbeddedCapacity] 命令。</span><span class="sxs-lookup"><span data-stu-id="aabed-138">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="aabed-139">筆記</span><span class="sxs-lookup"><span data-stu-id="aabed-139">NOTES</span></span>

## <span data-ttu-id="aabed-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="aabed-140">RELATED LINKS</span></span>

[<span data-ttu-id="aabed-141">AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="aabed-141">Get-AzureRmPowerBIEmbeddedCapacity</span></span>](./Get-AzureRmPowerBIEmbeddedCapacity.md)

[<span data-ttu-id="aabed-142">移除-AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="aabed-142">Remove-AzureRmPowerBIEmbeddedCapacity</span></span>](./Remove-AzureRmPowerBIEmbeddedCapacity.md)
