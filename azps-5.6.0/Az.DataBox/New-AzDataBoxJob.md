---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBox.dll-Help.xml
Module Name: Az.DataBox
online version: https://docs.microsoft.com/powershell/module/az.databox/new-azdataboxjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBox/DataBox/help/New-AzDataBoxJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBox/DataBox/help/New-AzDataBoxJob.md
ms.openlocfilehash: 2c78f8b40621ba58b84169f2bd9022399fce80b7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101914102"
---
# <span data-ttu-id="15c1c-101">New-AzDataBoxJob</span><span class="sxs-lookup"><span data-stu-id="15c1c-101">New-AzDataBoxJob</span></span>

## <span data-ttu-id="15c1c-102">簡介</span><span class="sxs-lookup"><span data-stu-id="15c1c-102">SYNOPSIS</span></span>
<span data-ttu-id="15c1c-103">使用指定的參數建立新資料箱工作</span><span class="sxs-lookup"><span data-stu-id="15c1c-103">Creates a new databox job using the specified parameters</span></span>

## <span data-ttu-id="15c1c-104">語法</span><span class="sxs-lookup"><span data-stu-id="15c1c-104">SYNTAX</span></span>

```
New-AzDataBoxJob -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 -Location <String> [-AddressType <AddressType>] [-CompanyName <String>] -StreetAddress1 <String>
 [-StreetAddress2 <String>] [-StreetAddress3 <String>] -PostalCode <String> -City <String>
 -StateOrProvinceCode <String> -CountryCode <String> -EmailId <String[]> -PhoneNumber <String>
 -ContactName <String> -StorageAccountResourceId <String[]> -DataBoxType <String>
 [-ExpectedDataSizeInTeraBytes <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="15c1c-105">描述</span><span class="sxs-lookup"><span data-stu-id="15c1c-105">DESCRIPTION</span></span>
<span data-ttu-id="15c1c-106">**New-AzDataBoxJob** Cmdlet 用來指定建立工作所需的詳細資料，以建立新資料箱工作。</span><span class="sxs-lookup"><span data-stu-id="15c1c-106">The **New-AzDataBoxJob** cmdlet is used to create a new databox job by specifying the details required for the creation of the job.</span></span>

## <span data-ttu-id="15c1c-107">例子</span><span class="sxs-lookup"><span data-stu-id="15c1c-107">EXAMPLES</span></span>

### <span data-ttu-id="15c1c-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="15c1c-108">Example 1</span></span>
```powershell
PS C:\> $s1 = <Storage Account Resource Id>
PS C:\> New-AzDataBoxJob -Location 'WestUS' -StreetAddress1 '16 TOWNSEND ST' -PostalCode 94107 -City 'San Francisco' -StateOrProvinceCode 'CA' -CountryCode 'US' -EmailId 'abc@outlook.com' -PhoneNumber 1234567891 -ContactName 'John' -StorageAccount $s1 -DataBoxType DataBox -ResourceGroupName TestRg -Name OrderTest

jobResource.Name jobResource.Sku.Name jobResource.Status jobResource.StartTime jobResource.Location ResourceGroup
---------------- -------------------- ------------------ --------------------- -------------------- -------------
OrderTest       DataBox              DeviceOrdered      05-07-2019 05:25:30   westus               TestRg
```

<span data-ttu-id="15c1c-109">Cmdlet 會採用所有必要的參數和一些選擇性參數來建立資料箱工作。</span><span class="sxs-lookup"><span data-stu-id="15c1c-109">The cmdlet takes all the required parameters and some optional parameters to create the databox job.</span></span>

## <span data-ttu-id="15c1c-110">參數</span><span class="sxs-lookup"><span data-stu-id="15c1c-110">PARAMETERS</span></span>

### <span data-ttu-id="15c1c-111">-AddressType</span><span class="sxs-lookup"><span data-stu-id="15c1c-111">-AddressType</span></span>
<span data-ttu-id="15c1c-112">網址類別型。</span><span class="sxs-lookup"><span data-stu-id="15c1c-112">Type of Address.</span></span> <span data-ttu-id="15c1c-113">可用值：AddressType.none (預設) 、AddressType.一、AddressType.Commercial</span><span class="sxs-lookup"><span data-stu-id="15c1c-113">Available values : AddressType.None (default), AddressType.Residential, AddressType.Commercial</span></span>

```yaml
Type: Microsoft.Azure.Management.DataBox.Models.AddressType
Parameter Sets: (All)
Aliases:
Accepted values: None, Residential, Commercial

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15c1c-114">-縣/市</span><span class="sxs-lookup"><span data-stu-id="15c1c-114">-City</span></span>
<span data-ttu-id="15c1c-115">縣/市名稱。</span><span class="sxs-lookup"><span data-stu-id="15c1c-115">Name of the City.</span></span> <span data-ttu-id="15c1c-116">例如：聖迭斯</span><span class="sxs-lookup"><span data-stu-id="15c1c-116">Ex : San Francisco</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15c1c-117">-CompanyName</span><span class="sxs-lookup"><span data-stu-id="15c1c-117">-CompanyName</span></span>
<span data-ttu-id="15c1c-118">公司名稱</span><span class="sxs-lookup"><span data-stu-id="15c1c-118">Name of the company</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15c1c-119">-ContactName</span><span class="sxs-lookup"><span data-stu-id="15c1c-119">-ContactName</span></span>
<span data-ttu-id="15c1c-120">連絡人名稱</span><span class="sxs-lookup"><span data-stu-id="15c1c-120">Contact Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15c1c-121">-CountryCode</span><span class="sxs-lookup"><span data-stu-id="15c1c-121">-CountryCode</span></span>
<span data-ttu-id="15c1c-122">國碼。</span><span class="sxs-lookup"><span data-stu-id="15c1c-122">Country Code.</span></span> <span data-ttu-id="15c1c-123">例如：美國</span><span class="sxs-lookup"><span data-stu-id="15c1c-123">Ex: US</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15c1c-124">-DataBoxType</span><span class="sxs-lookup"><span data-stu-id="15c1c-124">-DataBoxType</span></span>
<span data-ttu-id="15c1c-125">資料盒的 SKU 類型。</span><span class="sxs-lookup"><span data-stu-id="15c1c-125">Sku type of Databox.</span></span>  <span data-ttu-id="15c1c-126">可用值：DataBoxBox、Databox、DataBoxHeavy</span><span class="sxs-lookup"><span data-stu-id="15c1c-126">Available values : DataBoxDisk, Databox, DataBoxHeavy</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: DataBoxDisk, Databox, DataBoxHeavy

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15c1c-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="15c1c-127">-DefaultProfile</span></span>
<span data-ttu-id="15c1c-128">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="15c1c-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="15c1c-129">-EmailId</span><span class="sxs-lookup"><span data-stu-id="15c1c-129">-EmailId</span></span>
<span data-ttu-id="15c1c-130">您可以提供 EmailId 清單。</span><span class="sxs-lookup"><span data-stu-id="15c1c-130">List of EmailIds can be provided.</span></span> <span data-ttu-id="15c1c-131">至少必須一個</span><span class="sxs-lookup"><span data-stu-id="15c1c-131">Atleast one is mandatory</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15c1c-132">-ExpectedDataSizeInTeraBytes</span><span class="sxs-lookup"><span data-stu-id="15c1c-132">-ExpectedDataSizeInTeraBytes</span></span>
<span data-ttu-id="15c1c-133">針對 DataBoxBox 順序，以 TB 為單位指定預期資料是必填專案。</span><span class="sxs-lookup"><span data-stu-id="15c1c-133">For DataBoxDisk order, specifying the expected data in terabytes is mandatory.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15c1c-134">-位置</span><span class="sxs-lookup"><span data-stu-id="15c1c-134">-Location</span></span>
<span data-ttu-id="15c1c-135">訂閱的位置</span><span class="sxs-lookup"><span data-stu-id="15c1c-135">Location of the subscription</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15c1c-136">-名稱</span><span class="sxs-lookup"><span data-stu-id="15c1c-136">-Name</span></span>
<span data-ttu-id="15c1c-137">要建立的資料箱工作名稱</span><span class="sxs-lookup"><span data-stu-id="15c1c-137">Name of the databox job to be created</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15c1c-138">-PhoneNumber</span><span class="sxs-lookup"><span data-stu-id="15c1c-138">-PhoneNumber</span></span>
<span data-ttu-id="15c1c-139">連絡人號碼</span><span class="sxs-lookup"><span data-stu-id="15c1c-139">Contact Number</span></span> 

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15c1c-140">-PostalCode</span><span class="sxs-lookup"><span data-stu-id="15c1c-140">-PostalCode</span></span>
<span data-ttu-id="15c1c-141">郵遞區號</span><span class="sxs-lookup"><span data-stu-id="15c1c-141">Postal Code</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15c1c-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="15c1c-142">-ResourceGroupName</span></span>
<span data-ttu-id="15c1c-143">必須建立資料箱工作的資源組名。</span><span class="sxs-lookup"><span data-stu-id="15c1c-143">Resource Group Name under which the databox job has to be created.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15c1c-144">-StateOrProvinceCode</span><span class="sxs-lookup"><span data-stu-id="15c1c-144">-StateOrProvinceCode</span></span>
<span data-ttu-id="15c1c-145">輸入省/市代碼。</span><span class="sxs-lookup"><span data-stu-id="15c1c-145">Input the state or province code.</span></span> <span data-ttu-id="15c1c-146">Like CA - California;FL - 美國達裡達;紐約 - 紐約</span><span class="sxs-lookup"><span data-stu-id="15c1c-146">Like CA - California; FL - Florida; NY - New York</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15c1c-147">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="15c1c-147">-StorageAccountResourceId</span></span>
<span data-ttu-id="15c1c-148">儲存空間帳戶的資源識別碼清單。</span><span class="sxs-lookup"><span data-stu-id="15c1c-148">List of Resource Ids of Storage Accounts.</span></span> <span data-ttu-id="15c1c-149">至少必須一個。</span><span class="sxs-lookup"><span data-stu-id="15c1c-149">Atleast one is mandatory.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="15c1c-150">-StreetAddress1</span><span class="sxs-lookup"><span data-stu-id="15c1c-150">-StreetAddress1</span></span>
<span data-ttu-id="15c1c-151">街地道地道</span><span class="sxs-lookup"><span data-stu-id="15c1c-151">Street Address</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15c1c-152">-StreetAddress2</span><span class="sxs-lookup"><span data-stu-id="15c1c-152">-StreetAddress2</span></span>
<span data-ttu-id="15c1c-153">其他街地道號</span><span class="sxs-lookup"><span data-stu-id="15c1c-153">Additional Street Address</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15c1c-154">-StreetAddress3</span><span class="sxs-lookup"><span data-stu-id="15c1c-154">-StreetAddress3</span></span>
<span data-ttu-id="15c1c-155">其他街地道號</span><span class="sxs-lookup"><span data-stu-id="15c1c-155">Additional Street Address</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15c1c-156">-確認</span><span class="sxs-lookup"><span data-stu-id="15c1c-156">-Confirm</span></span>
<span data-ttu-id="15c1c-157">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="15c1c-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="15c1c-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="15c1c-158">-WhatIf</span></span>
<span data-ttu-id="15c1c-159">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="15c1c-159">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="15c1c-160">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="15c1c-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="15c1c-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15c1c-161">CommonParameters</span></span>
<span data-ttu-id="15c1c-162">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="15c1c-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15c1c-163">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="15c1c-163">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15c1c-164">輸入</span><span class="sxs-lookup"><span data-stu-id="15c1c-164">INPUTS</span></span>

### <span data-ttu-id="15c1c-165">System.String[]</span><span class="sxs-lookup"><span data-stu-id="15c1c-165">System.String[]</span></span>

## <span data-ttu-id="15c1c-166">輸出</span><span class="sxs-lookup"><span data-stu-id="15c1c-166">OUTPUTS</span></span>

### <span data-ttu-id="15c1c-167">Microsoft.Azure.PowerShell.Cmdlets.DataBox.Models.PSDataBoxJob</span><span class="sxs-lookup"><span data-stu-id="15c1c-167">Microsoft.Azure.PowerShell.Cmdlets.DataBox.Models.PSDataBoxJob</span></span>

## <span data-ttu-id="15c1c-168">筆記</span><span class="sxs-lookup"><span data-stu-id="15c1c-168">NOTES</span></span>

## <span data-ttu-id="15c1c-169">相關連結</span><span class="sxs-lookup"><span data-stu-id="15c1c-169">RELATED LINKS</span></span>
