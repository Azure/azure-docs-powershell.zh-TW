---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/new-azstackedgeorder
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeOrder.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeOrder.md
ms.openlocfilehash: a39986404e0969de2db4a2b58e0d275e102799cf
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93959012"
---
# <span data-ttu-id="c9ac9-101">New-AzStackEdgeOrder</span><span class="sxs-lookup"><span data-stu-id="c9ac9-101">New-AzStackEdgeOrder</span></span>

## <span data-ttu-id="c9ac9-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c9ac9-102">SYNOPSIS</span></span>
<span data-ttu-id="c9ac9-103">為裝置建立新的訂單。</span><span class="sxs-lookup"><span data-stu-id="c9ac9-103">Creates a new order for a device.</span></span>

## <span data-ttu-id="c9ac9-104">句法</span><span class="sxs-lookup"><span data-stu-id="c9ac9-104">SYNTAX</span></span>

```
New-AzStackEdgeOrder [-ResourceGroupName] <String> [-DeviceName] <String> -ContactPerson <String>
 -CompanyName <String> -Phone <String> -Email <String[]> -AddressLine1 <String> -PostalCode <String>
 -City <String> -State <String> -Country <String> [-AddressLine2 <String>] [-AddressLine3 <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c9ac9-105">說明</span><span class="sxs-lookup"><span data-stu-id="c9ac9-105">DESCRIPTION</span></span>
<span data-ttu-id="c9ac9-106">**新的-AzStackEdgeOrder** Cmdlet 會針對堆疊 Edge 裝置建立新的訂單。</span><span class="sxs-lookup"><span data-stu-id="c9ac9-106">The **New-AzStackEdgeOrder** cmdlet creates a new order for a Stack Edge device.</span></span> <span data-ttu-id="c9ac9-107">在建立訂單前，必須先建立堆疊邊緣裝置資源。</span><span class="sxs-lookup"><span data-stu-id="c9ac9-107">A Stack Edge device resource needs to be created first before creating an order.</span></span> <span data-ttu-id="c9ac9-108">您可以指定 [連絡人]、[公司名稱]、[電子郵件]、[位址等] 等詳細資料。作為建立訂單的參數。</span><span class="sxs-lookup"><span data-stu-id="c9ac9-108">You can specify details like contact person, company name, email, address etc. as parameters for creating the order.�</span></span>

## <span data-ttu-id="c9ac9-109">示例</span><span class="sxs-lookup"><span data-stu-id="c9ac9-109">EXAMPLES</span></span>

### <span data-ttu-id="c9ac9-110">範例1</span><span class="sxs-lookup"><span data-stu-id="c9ac9-110">Example 1</span></span>
```powershell
PS C:\> New-AzStackEdgeOrder -ResourceGroupName rg-name -DeviceName device-name -ContactPerson "John Mcclane" -CompanyName Microsoft -Phone 8004269400 -Email john@microsoft.com -AddressLine1  "Microsoft Corporation" -PostalCode 98052 -City Redmond -State WA -Country USA
DeviceName  ResourceGroupName Status    UpdatedDatetime
----------  ----------------- ------    ---------------
deviceName  resourceGroupName Untracked 01-Jan-01 12:00:00 AM
```

## <span data-ttu-id="c9ac9-111">參數</span><span class="sxs-lookup"><span data-stu-id="c9ac9-111">PARAMETERS</span></span>

### <span data-ttu-id="c9ac9-112">-AddressLine1</span><span class="sxs-lookup"><span data-stu-id="c9ac9-112">-AddressLine1</span></span>
<span data-ttu-id="c9ac9-113">[第一行位址]</span><span class="sxs-lookup"><span data-stu-id="c9ac9-113">Address first line</span></span>

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

### <span data-ttu-id="c9ac9-114">-AddressLine2</span><span class="sxs-lookup"><span data-stu-id="c9ac9-114">-AddressLine2</span></span>
<span data-ttu-id="c9ac9-115">位址第二行</span><span class="sxs-lookup"><span data-stu-id="c9ac9-115">Address second line</span></span>

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

### <span data-ttu-id="c9ac9-116">-AddressLine3</span><span class="sxs-lookup"><span data-stu-id="c9ac9-116">-AddressLine3</span></span>
<span data-ttu-id="c9ac9-117">第三行位址</span><span class="sxs-lookup"><span data-stu-id="c9ac9-117">Address third line</span></span>

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

### <span data-ttu-id="c9ac9-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c9ac9-118">-AsJob</span></span>
<span data-ttu-id="c9ac9-119">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="c9ac9-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c9ac9-120">-城市</span><span class="sxs-lookup"><span data-stu-id="c9ac9-120">-City</span></span>
<span data-ttu-id="c9ac9-121">城市名稱</span><span class="sxs-lookup"><span data-stu-id="c9ac9-121">Name of the City</span></span>

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

### <span data-ttu-id="c9ac9-122">-公司名稱</span><span class="sxs-lookup"><span data-stu-id="c9ac9-122">-CompanyName</span></span>
<span data-ttu-id="c9ac9-123">公司名稱</span><span class="sxs-lookup"><span data-stu-id="c9ac9-123">Name of the company</span></span>

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

### <span data-ttu-id="c9ac9-124">-ContactPerson</span><span class="sxs-lookup"><span data-stu-id="c9ac9-124">-ContactPerson</span></span>
<span data-ttu-id="c9ac9-125">連絡人的名稱</span><span class="sxs-lookup"><span data-stu-id="c9ac9-125">Name of the contact person</span></span>

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

### <span data-ttu-id="c9ac9-126">-國家/地區</span><span class="sxs-lookup"><span data-stu-id="c9ac9-126">-Country</span></span>
<span data-ttu-id="c9ac9-127">國家/地區的名稱</span><span class="sxs-lookup"><span data-stu-id="c9ac9-127">Name of the Country</span></span>

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

### <span data-ttu-id="c9ac9-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9ac9-128">-DefaultProfile</span></span>
<span data-ttu-id="c9ac9-129">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="c9ac9-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c9ac9-130">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="c9ac9-130">-DeviceName</span></span>
<span data-ttu-id="c9ac9-131">資源名稱</span><span class="sxs-lookup"><span data-stu-id="c9ac9-131">Resource Name</span></span>

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

### <span data-ttu-id="c9ac9-132">-電子郵件</span><span class="sxs-lookup"><span data-stu-id="c9ac9-132">-Email</span></span>
<span data-ttu-id="c9ac9-133">接收更新的電子郵件清單，接受最多10封電子郵件</span><span class="sxs-lookup"><span data-stu-id="c9ac9-133">List of Emails to receive updates, Accepts max of 10 emails</span></span>

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

### <span data-ttu-id="c9ac9-134">-電話</span><span class="sxs-lookup"><span data-stu-id="c9ac9-134">-Phone</span></span>
<span data-ttu-id="c9ac9-135">連絡人的電話號碼</span><span class="sxs-lookup"><span data-stu-id="c9ac9-135">Phone number of the contact person</span></span>

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

### <span data-ttu-id="c9ac9-136">-郵遞區號</span><span class="sxs-lookup"><span data-stu-id="c9ac9-136">-PostalCode</span></span>
<span data-ttu-id="c9ac9-137">位址的郵遞區號</span><span class="sxs-lookup"><span data-stu-id="c9ac9-137">Postal Code of the Address</span></span>

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

### <span data-ttu-id="c9ac9-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c9ac9-138">-ResourceGroupName</span></span>
<span data-ttu-id="c9ac9-139">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="c9ac9-139">Resource Group Name</span></span>

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

### <span data-ttu-id="c9ac9-140">-State</span><span class="sxs-lookup"><span data-stu-id="c9ac9-140">-State</span></span>
<span data-ttu-id="c9ac9-141">狀態的名稱</span><span class="sxs-lookup"><span data-stu-id="c9ac9-141">Name of the State</span></span>

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

### <span data-ttu-id="c9ac9-142">-確認</span><span class="sxs-lookup"><span data-stu-id="c9ac9-142">-Confirm</span></span>
<span data-ttu-id="c9ac9-143">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="c9ac9-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c9ac9-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c9ac9-144">-WhatIf</span></span>
<span data-ttu-id="c9ac9-145">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="c9ac9-145">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c9ac9-146">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c9ac9-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c9ac9-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9ac9-147">CommonParameters</span></span>
<span data-ttu-id="c9ac9-148">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c9ac9-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9ac9-149">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="c9ac9-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9ac9-150">輸入</span><span class="sxs-lookup"><span data-stu-id="c9ac9-150">INPUTS</span></span>

### <span data-ttu-id="c9ac9-151">System.object</span><span class="sxs-lookup"><span data-stu-id="c9ac9-151">System.String</span></span>

## <span data-ttu-id="c9ac9-152">輸出</span><span class="sxs-lookup"><span data-stu-id="c9ac9-152">OUTPUTS</span></span>

### <span data-ttu-id="c9ac9-153">PSStackEdgeOrder （StackEdge）的</span><span class="sxs-lookup"><span data-stu-id="c9ac9-153">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeOrder</span></span>

## <span data-ttu-id="c9ac9-154">筆記</span><span class="sxs-lookup"><span data-stu-id="c9ac9-154">NOTES</span></span>

## <span data-ttu-id="c9ac9-155">相關連結</span><span class="sxs-lookup"><span data-stu-id="c9ac9-155">RELATED LINKS</span></span>
