---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/new-azdataboxedgeorder
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeOrder.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeOrder.md
ms.openlocfilehash: 4b8bd90cd96654fa137301379dceaabccad8a2ea
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98449463"
---
# <span data-ttu-id="2aaf2-101">New-AzDataBoxEdgeOrder</span><span class="sxs-lookup"><span data-stu-id="2aaf2-101">New-AzDataBoxEdgeOrder</span></span>

## <span data-ttu-id="2aaf2-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2aaf2-102">SYNOPSIS</span></span>
<span data-ttu-id="2aaf2-103">為裝置建立新的訂單。</span><span class="sxs-lookup"><span data-stu-id="2aaf2-103">Creates a new order for a device.</span></span>

## <span data-ttu-id="2aaf2-104">句法</span><span class="sxs-lookup"><span data-stu-id="2aaf2-104">SYNTAX</span></span>

```
New-AzDataBoxEdgeOrder [-ResourceGroupName] <String> [-DeviceName] <String> -ContactPerson <String>
 -CompanyName <String> -Phone <String> -Email <String[]> -AddressLine1 <String> -PostalCode <String>
 -City <String> -State <String> -Country <String> [-AddressLine2 <String>] [-AddressLine3 <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2aaf2-105">說明</span><span class="sxs-lookup"><span data-stu-id="2aaf2-105">DESCRIPTION</span></span>
<span data-ttu-id="2aaf2-106">**AzDataBoxEdgeOrder** Cmdlet 會針對資料編輯方塊邊緣裝置建立新的訂單。</span><span class="sxs-lookup"><span data-stu-id="2aaf2-106">The **New-AzDataBoxEdgeOrder** cmdlet creates a new order for a Data Box Edge device.</span></span> <span data-ttu-id="2aaf2-107">建立訂單前，必須先建立資料編輯方塊邊緣裝置資源。</span><span class="sxs-lookup"><span data-stu-id="2aaf2-107">A Data Box Edge device resource needs to be created first before creating an order.</span></span> <span data-ttu-id="2aaf2-108">您可以指定 [連絡人]、[公司名稱]、[電子郵件]、[位址等] 等詳細資料。作為建立訂單的參數。</span><span class="sxs-lookup"><span data-stu-id="2aaf2-108">You can specify details like contact person, company name, email, address etc. as parameters for creating the order.�</span></span>

## <span data-ttu-id="2aaf2-109">示例</span><span class="sxs-lookup"><span data-stu-id="2aaf2-109">EXAMPLES</span></span>

### <span data-ttu-id="2aaf2-110">範例1</span><span class="sxs-lookup"><span data-stu-id="2aaf2-110">Example 1</span></span>
```powershell
PS C:\> New-AzDataBoxEdgeOrder -ResourceGroupName rg-name -DeviceName device-name -ContactPerson "John Mcclane" -CompanyName Microsoft -Phone 8004269400 -Email john@microsoft.com -AddressLine1  "Microsoft Corporation" -PostalCode 98052 -City Redmond -State WA -Country USA
DeviceName  ResourceGroupName Status    UpdatedDatetime
----------  ----------------- ------    ---------------
deviceName  resourceGroupName Untracked 01-Jan-01 12:00:00 AM
```

## <span data-ttu-id="2aaf2-111">參數</span><span class="sxs-lookup"><span data-stu-id="2aaf2-111">PARAMETERS</span></span>

### <span data-ttu-id="2aaf2-112">-AddressLine1</span><span class="sxs-lookup"><span data-stu-id="2aaf2-112">-AddressLine1</span></span>
<span data-ttu-id="2aaf2-113">[第一行位址]</span><span class="sxs-lookup"><span data-stu-id="2aaf2-113">Address first line</span></span>

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

### <span data-ttu-id="2aaf2-114">-AddressLine2</span><span class="sxs-lookup"><span data-stu-id="2aaf2-114">-AddressLine2</span></span>
<span data-ttu-id="2aaf2-115">位址第二行</span><span class="sxs-lookup"><span data-stu-id="2aaf2-115">Address second line</span></span>

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

### <span data-ttu-id="2aaf2-116">-AddressLine3</span><span class="sxs-lookup"><span data-stu-id="2aaf2-116">-AddressLine3</span></span>
<span data-ttu-id="2aaf2-117">第三行位址</span><span class="sxs-lookup"><span data-stu-id="2aaf2-117">Address third line</span></span>

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

### <span data-ttu-id="2aaf2-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2aaf2-118">-AsJob</span></span>
<span data-ttu-id="2aaf2-119">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="2aaf2-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2aaf2-120">-城市</span><span class="sxs-lookup"><span data-stu-id="2aaf2-120">-City</span></span>
<span data-ttu-id="2aaf2-121">城市名稱</span><span class="sxs-lookup"><span data-stu-id="2aaf2-121">Name of the City</span></span>

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

### <span data-ttu-id="2aaf2-122">-公司名稱</span><span class="sxs-lookup"><span data-stu-id="2aaf2-122">-CompanyName</span></span>
<span data-ttu-id="2aaf2-123">公司名稱</span><span class="sxs-lookup"><span data-stu-id="2aaf2-123">Name of the company</span></span>

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

### <span data-ttu-id="2aaf2-124">-ContactPerson</span><span class="sxs-lookup"><span data-stu-id="2aaf2-124">-ContactPerson</span></span>
<span data-ttu-id="2aaf2-125">連絡人的名稱</span><span class="sxs-lookup"><span data-stu-id="2aaf2-125">Name of the contact person</span></span>

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

### <span data-ttu-id="2aaf2-126">-國家/地區</span><span class="sxs-lookup"><span data-stu-id="2aaf2-126">-Country</span></span>
<span data-ttu-id="2aaf2-127">國家/地區的名稱</span><span class="sxs-lookup"><span data-stu-id="2aaf2-127">Name of the Country</span></span>

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

### <span data-ttu-id="2aaf2-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2aaf2-128">-DefaultProfile</span></span>
<span data-ttu-id="2aaf2-129">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="2aaf2-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2aaf2-130">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="2aaf2-130">-DeviceName</span></span>
<span data-ttu-id="2aaf2-131">資源名稱</span><span class="sxs-lookup"><span data-stu-id="2aaf2-131">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2aaf2-132">-電子郵件</span><span class="sxs-lookup"><span data-stu-id="2aaf2-132">-Email</span></span>
<span data-ttu-id="2aaf2-133">接收更新的電子郵件清單，接受最多10封電子郵件</span><span class="sxs-lookup"><span data-stu-id="2aaf2-133">List of Emails to receive updates, Accepts max of 10 emails</span></span>

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

### <span data-ttu-id="2aaf2-134">-電話</span><span class="sxs-lookup"><span data-stu-id="2aaf2-134">-Phone</span></span>
<span data-ttu-id="2aaf2-135">連絡人的電話號碼</span><span class="sxs-lookup"><span data-stu-id="2aaf2-135">Phone number of the contact person</span></span>

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

### <span data-ttu-id="2aaf2-136">-郵遞區號</span><span class="sxs-lookup"><span data-stu-id="2aaf2-136">-PostalCode</span></span>
<span data-ttu-id="2aaf2-137">位址的郵遞區號</span><span class="sxs-lookup"><span data-stu-id="2aaf2-137">Postal Code of the Address</span></span>

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

### <span data-ttu-id="2aaf2-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2aaf2-138">-ResourceGroupName</span></span>
<span data-ttu-id="2aaf2-139">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="2aaf2-139">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2aaf2-140">-State</span><span class="sxs-lookup"><span data-stu-id="2aaf2-140">-State</span></span>
<span data-ttu-id="2aaf2-141">狀態的名稱</span><span class="sxs-lookup"><span data-stu-id="2aaf2-141">Name of the State</span></span>

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

### <span data-ttu-id="2aaf2-142">-確認</span><span class="sxs-lookup"><span data-stu-id="2aaf2-142">-Confirm</span></span>
<span data-ttu-id="2aaf2-143">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="2aaf2-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2aaf2-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2aaf2-144">-WhatIf</span></span>
<span data-ttu-id="2aaf2-145">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="2aaf2-145">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2aaf2-146">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="2aaf2-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2aaf2-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2aaf2-147">CommonParameters</span></span>
<span data-ttu-id="2aaf2-148">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="2aaf2-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2aaf2-149">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="2aaf2-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2aaf2-150">輸入</span><span class="sxs-lookup"><span data-stu-id="2aaf2-150">INPUTS</span></span>

### <span data-ttu-id="2aaf2-151">System.object</span><span class="sxs-lookup"><span data-stu-id="2aaf2-151">System.String</span></span>

## <span data-ttu-id="2aaf2-152">輸出</span><span class="sxs-lookup"><span data-stu-id="2aaf2-152">OUTPUTS</span></span>

### <span data-ttu-id="2aaf2-153">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeOrder</span><span class="sxs-lookup"><span data-stu-id="2aaf2-153">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeOrder</span></span>

## <span data-ttu-id="2aaf2-154">筆記</span><span class="sxs-lookup"><span data-stu-id="2aaf2-154">NOTES</span></span>

## <span data-ttu-id="2aaf2-155">相關連結</span><span class="sxs-lookup"><span data-stu-id="2aaf2-155">RELATED LINKS</span></span>
