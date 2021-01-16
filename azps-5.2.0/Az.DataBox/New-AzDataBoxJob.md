---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBox.dll-Help.xml
Module Name: Az.DataBox
online version: https://docs.microsoft.com/en-us/powershell/module/az.databox/new-azdataboxjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBox/DataBox/help/New-AzDataBoxJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBox/DataBox/help/New-AzDataBoxJob.md
ms.openlocfilehash: 4402eaed4b76ce6e769141748b043598bdfd099a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98280674"
---
# <span data-ttu-id="3bb0c-101">New-AzDataBoxJob</span><span class="sxs-lookup"><span data-stu-id="3bb0c-101">New-AzDataBoxJob</span></span>

## <span data-ttu-id="3bb0c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="3bb0c-102">SYNOPSIS</span></span>
<span data-ttu-id="3bb0c-103">使用指定的參數建立新的 databox 工作</span><span class="sxs-lookup"><span data-stu-id="3bb0c-103">Creates a new databox job using the specified parameters</span></span>

## <span data-ttu-id="3bb0c-104">句法</span><span class="sxs-lookup"><span data-stu-id="3bb0c-104">SYNTAX</span></span>

```
New-AzDataBoxJob -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 -Location <String> [-AddressType <AddressType>] [-CompanyName <String>] -StreetAddress1 <String>
 [-StreetAddress2 <String>] [-StreetAddress3 <String>] -PostalCode <String> -City <String>
 -StateOrProvinceCode <String> -CountryCode <String> -EmailId <String[]> -PhoneNumber <String>
 -ContactName <String> -StorageAccountResourceId <String[]> -DataBoxType <String>
 [-ExpectedDataSizeInTeraBytes <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3bb0c-105">說明</span><span class="sxs-lookup"><span data-stu-id="3bb0c-105">DESCRIPTION</span></span>
<span data-ttu-id="3bb0c-106">**新的-AzDataBoxJob** Cmdlet 是用來建立工作所需的詳細資料，以建立新的 databox 作業。</span><span class="sxs-lookup"><span data-stu-id="3bb0c-106">The **New-AzDataBoxJob** cmdlet is used to create a new databox job by specifying the details required for the creation of the job.</span></span>

## <span data-ttu-id="3bb0c-107">示例</span><span class="sxs-lookup"><span data-stu-id="3bb0c-107">EXAMPLES</span></span>

### <span data-ttu-id="3bb0c-108">範例1</span><span class="sxs-lookup"><span data-stu-id="3bb0c-108">Example 1</span></span>
```powershell
PS C:\> $s1 = <Storage Account Resource Id>
PS C:\> New-AzDataBoxJob -Location 'WestUS' -StreetAddress1 '16 TOWNSEND ST' -PostalCode 94107 -City 'San Francisco' -StateOrProvinceCode 'CA' -CountryCode 'US' -EmailId 'abc@outlook.com' -PhoneNumber 1234567891 -ContactName 'John' -StorageAccount $s1 -DataBoxType DataBox -ResourceGroupName TestRg -Name OrderTest

jobResource.Name jobResource.Sku.Name jobResource.Status jobResource.StartTime jobResource.Location ResourceGroup
---------------- -------------------- ------------------ --------------------- -------------------- -------------
OrderTest       DataBox              DeviceOrdered      05-07-2019 05:25:30   westus               TestRg
```

<span data-ttu-id="3bb0c-109">這個 Cmdlet 會採用所有必要的參數和一些選用的參數來建立 databox 工作。</span><span class="sxs-lookup"><span data-stu-id="3bb0c-109">The cmdlet takes all the required parameters and some optional parameters to create the databox job.</span></span>

## <span data-ttu-id="3bb0c-110">參數</span><span class="sxs-lookup"><span data-stu-id="3bb0c-110">PARAMETERS</span></span>

### <span data-ttu-id="3bb0c-111">-AddressType</span><span class="sxs-lookup"><span data-stu-id="3bb0c-111">-AddressType</span></span>
<span data-ttu-id="3bb0c-112">網址類別型。</span><span class="sxs-lookup"><span data-stu-id="3bb0c-112">Type of Address.</span></span> <span data-ttu-id="3bb0c-113">可用值： AddressType (預設) 、AddressType、AddressType、商業版</span><span class="sxs-lookup"><span data-stu-id="3bb0c-113">Available values : AddressType.None (default), AddressType.Residential, AddressType.Commercial</span></span>

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

### <span data-ttu-id="3bb0c-114">-城市</span><span class="sxs-lookup"><span data-stu-id="3bb0c-114">-City</span></span>
<span data-ttu-id="3bb0c-115">城市的名稱。</span><span class="sxs-lookup"><span data-stu-id="3bb0c-115">Name of the City.</span></span> <span data-ttu-id="3bb0c-116">Ex：三藩市</span><span class="sxs-lookup"><span data-stu-id="3bb0c-116">Ex : San Francisco</span></span>

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

### <span data-ttu-id="3bb0c-117">-公司名稱</span><span class="sxs-lookup"><span data-stu-id="3bb0c-117">-CompanyName</span></span>
<span data-ttu-id="3bb0c-118">公司名稱</span><span class="sxs-lookup"><span data-stu-id="3bb0c-118">Name of the company</span></span>

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

### <span data-ttu-id="3bb0c-119">-連絡人姓名</span><span class="sxs-lookup"><span data-stu-id="3bb0c-119">-ContactName</span></span>
<span data-ttu-id="3bb0c-120">連絡人名稱</span><span class="sxs-lookup"><span data-stu-id="3bb0c-120">Contact Name</span></span>

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

### <span data-ttu-id="3bb0c-121">-CountryCode</span><span class="sxs-lookup"><span data-stu-id="3bb0c-121">-CountryCode</span></span>
<span data-ttu-id="3bb0c-122">國家/地區碼。</span><span class="sxs-lookup"><span data-stu-id="3bb0c-122">Country Code.</span></span> <span data-ttu-id="3bb0c-123">Ex：美國</span><span class="sxs-lookup"><span data-stu-id="3bb0c-123">Ex: US</span></span>

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

### <span data-ttu-id="3bb0c-124">-DataBoxType</span><span class="sxs-lookup"><span data-stu-id="3bb0c-124">-DataBoxType</span></span>
<span data-ttu-id="3bb0c-125">Databox 的 Sku 類型。</span><span class="sxs-lookup"><span data-stu-id="3bb0c-125">Sku type of Databox.</span></span>  <span data-ttu-id="3bb0c-126">可用值： DataBoxDisk、Databox、DataBoxHeavy</span><span class="sxs-lookup"><span data-stu-id="3bb0c-126">Available values : DataBoxDisk, Databox, DataBoxHeavy</span></span>

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

### <span data-ttu-id="3bb0c-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3bb0c-127">-DefaultProfile</span></span>
<span data-ttu-id="3bb0c-128">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="3bb0c-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3bb0c-129">-EmailId</span><span class="sxs-lookup"><span data-stu-id="3bb0c-129">-EmailId</span></span>
<span data-ttu-id="3bb0c-130">可提供 EmailIds 清單。</span><span class="sxs-lookup"><span data-stu-id="3bb0c-130">List of EmailIds can be provided.</span></span> <span data-ttu-id="3bb0c-131">必須至少有一個專案</span><span class="sxs-lookup"><span data-stu-id="3bb0c-131">Atleast one is mandatory</span></span>

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

### <span data-ttu-id="3bb0c-132">-ExpectedDataSizeInTeraBytes</span><span class="sxs-lookup"><span data-stu-id="3bb0c-132">-ExpectedDataSizeInTeraBytes</span></span>
<span data-ttu-id="3bb0c-133">針對 DataBoxDisk 順序，指定預期資料的 tb 數是強制性的。</span><span class="sxs-lookup"><span data-stu-id="3bb0c-133">For DataBoxDisk order, specifying the expected data in terabytes is mandatory.</span></span>

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

### <span data-ttu-id="3bb0c-134">-位置</span><span class="sxs-lookup"><span data-stu-id="3bb0c-134">-Location</span></span>
<span data-ttu-id="3bb0c-135">訂閱的位置</span><span class="sxs-lookup"><span data-stu-id="3bb0c-135">Location of the subscription</span></span>

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

### <span data-ttu-id="3bb0c-136">-名稱</span><span class="sxs-lookup"><span data-stu-id="3bb0c-136">-Name</span></span>
<span data-ttu-id="3bb0c-137">要建立之 databox 作業的名稱</span><span class="sxs-lookup"><span data-stu-id="3bb0c-137">Name of the databox job to be created</span></span>

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

### <span data-ttu-id="3bb0c-138">-PhoneNumber</span><span class="sxs-lookup"><span data-stu-id="3bb0c-138">-PhoneNumber</span></span>
<span data-ttu-id="3bb0c-139">連絡人編號</span><span class="sxs-lookup"><span data-stu-id="3bb0c-139">Contact Number</span></span> 

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

### <span data-ttu-id="3bb0c-140">-郵遞區號</span><span class="sxs-lookup"><span data-stu-id="3bb0c-140">-PostalCode</span></span>
<span data-ttu-id="3bb0c-141">郵遞區號</span><span class="sxs-lookup"><span data-stu-id="3bb0c-141">Postal Code</span></span>

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

### <span data-ttu-id="3bb0c-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3bb0c-142">-ResourceGroupName</span></span>
<span data-ttu-id="3bb0c-143">您必須在其上建立 databox 作業的資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="3bb0c-143">Resource Group Name under which the databox job has to be created.</span></span>

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

### <span data-ttu-id="3bb0c-144">-StateOrProvinceCode</span><span class="sxs-lookup"><span data-stu-id="3bb0c-144">-StateOrProvinceCode</span></span>
<span data-ttu-id="3bb0c-145">輸入州或省份碼。</span><span class="sxs-lookup"><span data-stu-id="3bb0c-145">Input the state or province code.</span></span> <span data-ttu-id="3bb0c-146">贊 CA-加州;FL-佛羅里達。紐約州紐約市</span><span class="sxs-lookup"><span data-stu-id="3bb0c-146">Like CA - California; FL - Florida; NY - New York</span></span>

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

### <span data-ttu-id="3bb0c-147">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="3bb0c-147">-StorageAccountResourceId</span></span>
<span data-ttu-id="3bb0c-148">儲存空間帳戶的資源識別碼清單。</span><span class="sxs-lookup"><span data-stu-id="3bb0c-148">List of Resource Ids of Storage Accounts.</span></span> <span data-ttu-id="3bb0c-149">至少必須有一個。</span><span class="sxs-lookup"><span data-stu-id="3bb0c-149">Atleast one is mandatory.</span></span>

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

### <span data-ttu-id="3bb0c-150">-StreetAddress1</span><span class="sxs-lookup"><span data-stu-id="3bb0c-150">-StreetAddress1</span></span>
<span data-ttu-id="3bb0c-151">街道位址</span><span class="sxs-lookup"><span data-stu-id="3bb0c-151">Street Address</span></span>

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

### <span data-ttu-id="3bb0c-152">-StreetAddress2</span><span class="sxs-lookup"><span data-stu-id="3bb0c-152">-StreetAddress2</span></span>
<span data-ttu-id="3bb0c-153">其他街道位址</span><span class="sxs-lookup"><span data-stu-id="3bb0c-153">Additional Street Address</span></span>

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

### <span data-ttu-id="3bb0c-154">-StreetAddress3</span><span class="sxs-lookup"><span data-stu-id="3bb0c-154">-StreetAddress3</span></span>
<span data-ttu-id="3bb0c-155">其他街道位址</span><span class="sxs-lookup"><span data-stu-id="3bb0c-155">Additional Street Address</span></span>

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

### <span data-ttu-id="3bb0c-156">-確認</span><span class="sxs-lookup"><span data-stu-id="3bb0c-156">-Confirm</span></span>
<span data-ttu-id="3bb0c-157">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="3bb0c-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3bb0c-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3bb0c-158">-WhatIf</span></span>
<span data-ttu-id="3bb0c-159">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="3bb0c-159">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3bb0c-160">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="3bb0c-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3bb0c-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3bb0c-161">CommonParameters</span></span>
<span data-ttu-id="3bb0c-162">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="3bb0c-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3bb0c-163">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="3bb0c-163">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3bb0c-164">輸入</span><span class="sxs-lookup"><span data-stu-id="3bb0c-164">INPUTS</span></span>

### <span data-ttu-id="3bb0c-165">System.object []</span><span class="sxs-lookup"><span data-stu-id="3bb0c-165">System.String[]</span></span>

## <span data-ttu-id="3bb0c-166">輸出</span><span class="sxs-lookup"><span data-stu-id="3bb0c-166">OUTPUTS</span></span>

### <span data-ttu-id="3bb0c-167">Microsoft.Azure.PowerShell.Cmdlets.DataBox.Models.PSDataBoxJob</span><span class="sxs-lookup"><span data-stu-id="3bb0c-167">Microsoft.Azure.PowerShell.Cmdlets.DataBox.Models.PSDataBoxJob</span></span>

## <span data-ttu-id="3bb0c-168">筆記</span><span class="sxs-lookup"><span data-stu-id="3bb0c-168">NOTES</span></span>

## <span data-ttu-id="3bb0c-169">相關連結</span><span class="sxs-lookup"><span data-stu-id="3bb0c-169">RELATED LINKS</span></span>
