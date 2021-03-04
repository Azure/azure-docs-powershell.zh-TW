---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/powershell/module/az.stackedge/new-azstackedgeorder
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeOrder.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeOrder.md
ms.openlocfilehash: 4cb6c46f3cadae9d36ec273fe7d6198e35927c81
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101909418"
---
# <span data-ttu-id="f47f0-101">New-AzStackEdgeOrder</span><span class="sxs-lookup"><span data-stu-id="f47f0-101">New-AzStackEdgeOrder</span></span>

## <span data-ttu-id="f47f0-102">簡介</span><span class="sxs-lookup"><span data-stu-id="f47f0-102">SYNOPSIS</span></span>
<span data-ttu-id="f47f0-103">為裝置建立新訂單。</span><span class="sxs-lookup"><span data-stu-id="f47f0-103">Creates a new order for a device.</span></span>

## <span data-ttu-id="f47f0-104">語法</span><span class="sxs-lookup"><span data-stu-id="f47f0-104">SYNTAX</span></span>

```
New-AzStackEdgeOrder [-ResourceGroupName] <String> [-DeviceName] <String> -ContactPerson <String>
 -CompanyName <String> -Phone <String> -Email <String[]> -AddressLine1 <String> -PostalCode <String>
 -City <String> -State <String> -Country <String> [-AddressLine2 <String>] [-AddressLine3 <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f47f0-105">描述</span><span class="sxs-lookup"><span data-stu-id="f47f0-105">DESCRIPTION</span></span>
<span data-ttu-id="f47f0-106">**New-AzStackEdgeOrder** Cmdlet 會為 Stack Edge 裝置建立新訂單。</span><span class="sxs-lookup"><span data-stu-id="f47f0-106">The **New-AzStackEdgeOrder** cmdlet creates a new order for a Stack Edge device.</span></span> <span data-ttu-id="f47f0-107">在建立訂單之前，必須先建立 Stack Edge 裝置資源。</span><span class="sxs-lookup"><span data-stu-id="f47f0-107">A Stack Edge device resource needs to be created first before creating an order.</span></span> <span data-ttu-id="f47f0-108">您可以將連絡人、公司名稱、電子郵件、位址等詳細資料指定為建立訂單的參數。</span><span class="sxs-lookup"><span data-stu-id="f47f0-108">You can specify details like contact person, company name, email, address etc. as parameters for creating the order.�</span></span>

## <span data-ttu-id="f47f0-109">例子</span><span class="sxs-lookup"><span data-stu-id="f47f0-109">EXAMPLES</span></span>

### <span data-ttu-id="f47f0-110">範例 1</span><span class="sxs-lookup"><span data-stu-id="f47f0-110">Example 1</span></span>
```powershell
PS C:\> New-AzStackEdgeOrder -ResourceGroupName rg-name -DeviceName device-name -ContactPerson "John Mcclane" -CompanyName Microsoft -Phone 8004269400 -Email john@microsoft.com -AddressLine1  "Microsoft Corporation" -PostalCode 98052 -City Redmond -State WA -Country USA
DeviceName  ResourceGroupName Status    UpdatedDatetime
----------  ----------------- ------    ---------------
deviceName  resourceGroupName Untracked 01-Jan-01 12:00:00 AM
```

## <span data-ttu-id="f47f0-111">參數</span><span class="sxs-lookup"><span data-stu-id="f47f0-111">PARAMETERS</span></span>

### <span data-ttu-id="f47f0-112">-AddressLine1</span><span class="sxs-lookup"><span data-stu-id="f47f0-112">-AddressLine1</span></span>
<span data-ttu-id="f47f0-113">位址第一行</span><span class="sxs-lookup"><span data-stu-id="f47f0-113">Address first line</span></span>

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

### <span data-ttu-id="f47f0-114">-AddressLine2</span><span class="sxs-lookup"><span data-stu-id="f47f0-114">-AddressLine2</span></span>
<span data-ttu-id="f47f0-115">位址第二行</span><span class="sxs-lookup"><span data-stu-id="f47f0-115">Address second line</span></span>

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

### <span data-ttu-id="f47f0-116">-AddressLine3</span><span class="sxs-lookup"><span data-stu-id="f47f0-116">-AddressLine3</span></span>
<span data-ttu-id="f47f0-117">位址第三行</span><span class="sxs-lookup"><span data-stu-id="f47f0-117">Address third line</span></span>

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

### <span data-ttu-id="f47f0-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f47f0-118">-AsJob</span></span>
<span data-ttu-id="f47f0-119">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="f47f0-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f47f0-120">-縣/市</span><span class="sxs-lookup"><span data-stu-id="f47f0-120">-City</span></span>
<span data-ttu-id="f47f0-121">縣/市名稱</span><span class="sxs-lookup"><span data-stu-id="f47f0-121">Name of the City</span></span>

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

### <span data-ttu-id="f47f0-122">-CompanyName</span><span class="sxs-lookup"><span data-stu-id="f47f0-122">-CompanyName</span></span>
<span data-ttu-id="f47f0-123">公司名稱</span><span class="sxs-lookup"><span data-stu-id="f47f0-123">Name of the company</span></span>

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

### <span data-ttu-id="f47f0-124">-ContactPerson</span><span class="sxs-lookup"><span data-stu-id="f47f0-124">-ContactPerson</span></span>
<span data-ttu-id="f47f0-125">連絡人名稱</span><span class="sxs-lookup"><span data-stu-id="f47f0-125">Name of the contact person</span></span>

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

### <span data-ttu-id="f47f0-126">-國家/地區</span><span class="sxs-lookup"><span data-stu-id="f47f0-126">-Country</span></span>
<span data-ttu-id="f47f0-127">國家/地區名稱</span><span class="sxs-lookup"><span data-stu-id="f47f0-127">Name of the Country</span></span>

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

### <span data-ttu-id="f47f0-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f47f0-128">-DefaultProfile</span></span>
<span data-ttu-id="f47f0-129">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="f47f0-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f47f0-130">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="f47f0-130">-DeviceName</span></span>
<span data-ttu-id="f47f0-131">資源名稱</span><span class="sxs-lookup"><span data-stu-id="f47f0-131">Resource Name</span></span>

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

### <span data-ttu-id="f47f0-132">-電子郵件</span><span class="sxs-lookup"><span data-stu-id="f47f0-132">-Email</span></span>
<span data-ttu-id="f47f0-133">接收更新的電子郵件清單，最多接受 10 封電子郵件</span><span class="sxs-lookup"><span data-stu-id="f47f0-133">List of Emails to receive updates, Accepts max of 10 emails</span></span>

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

### <span data-ttu-id="f47f0-134">-電話</span><span class="sxs-lookup"><span data-stu-id="f47f0-134">-Phone</span></span>
<span data-ttu-id="f47f0-135">連絡人的電話號碼</span><span class="sxs-lookup"><span data-stu-id="f47f0-135">Phone number of the contact person</span></span>

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

### <span data-ttu-id="f47f0-136">-PostalCode</span><span class="sxs-lookup"><span data-stu-id="f47f0-136">-PostalCode</span></span>
<span data-ttu-id="f47f0-137">位址的郵遞區號</span><span class="sxs-lookup"><span data-stu-id="f47f0-137">Postal Code of the Address</span></span>

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

### <span data-ttu-id="f47f0-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f47f0-138">-ResourceGroupName</span></span>
<span data-ttu-id="f47f0-139">資源組名</span><span class="sxs-lookup"><span data-stu-id="f47f0-139">Resource Group Name</span></span>

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

### <span data-ttu-id="f47f0-140">-State</span><span class="sxs-lookup"><span data-stu-id="f47f0-140">-State</span></span>
<span data-ttu-id="f47f0-141">州名</span><span class="sxs-lookup"><span data-stu-id="f47f0-141">Name of the State</span></span>

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

### <span data-ttu-id="f47f0-142">-確認</span><span class="sxs-lookup"><span data-stu-id="f47f0-142">-Confirm</span></span>
<span data-ttu-id="f47f0-143">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="f47f0-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f47f0-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f47f0-144">-WhatIf</span></span>
<span data-ttu-id="f47f0-145">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="f47f0-145">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f47f0-146">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f47f0-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f47f0-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f47f0-147">CommonParameters</span></span>
<span data-ttu-id="f47f0-148">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="f47f0-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f47f0-149">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f47f0-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f47f0-150">輸入</span><span class="sxs-lookup"><span data-stu-id="f47f0-150">INPUTS</span></span>

### <span data-ttu-id="f47f0-151">System.String</span><span class="sxs-lookup"><span data-stu-id="f47f0-151">System.String</span></span>

## <span data-ttu-id="f47f0-152">輸出</span><span class="sxs-lookup"><span data-stu-id="f47f0-152">OUTPUTS</span></span>

### <span data-ttu-id="f47f0-153">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.models.PSStackEdgeOrder</span><span class="sxs-lookup"><span data-stu-id="f47f0-153">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeOrder</span></span>

## <span data-ttu-id="f47f0-154">筆記</span><span class="sxs-lookup"><span data-stu-id="f47f0-154">NOTES</span></span>

## <span data-ttu-id="f47f0-155">相關連結</span><span class="sxs-lookup"><span data-stu-id="f47f0-155">RELATED LINKS</span></span>
