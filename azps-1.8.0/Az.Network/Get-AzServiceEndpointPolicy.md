---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azserviceendpointpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzServiceEndpointPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzServiceEndpointPolicy.md
ms.openlocfilehash: fdff53931891ce62b2182f2c8c78d54312141f5c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93621942"
---
# <span data-ttu-id="8dc78-101">Get-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="8dc78-101">Get-AzServiceEndpointPolicy</span></span>

## <span data-ttu-id="8dc78-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8dc78-102">SYNOPSIS</span></span>
<span data-ttu-id="8dc78-103">取得服務端點原則。</span><span class="sxs-lookup"><span data-stu-id="8dc78-103">Gets a service endpoint policy.</span></span>

## <span data-ttu-id="8dc78-104">句法</span><span class="sxs-lookup"><span data-stu-id="8dc78-104">SYNTAX</span></span>

### <span data-ttu-id="8dc78-105">ListParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="8dc78-105">ListParameterSet (Default)</span></span>
```
Get-AzServiceEndpointPolicy [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8dc78-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8dc78-106">GetByResourceIdParameterSet</span></span>
```
Get-AzServiceEndpointPolicy -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8dc78-107">說明</span><span class="sxs-lookup"><span data-stu-id="8dc78-107">DESCRIPTION</span></span>
<span data-ttu-id="8dc78-108">**AzServiceEndpointPolicy** Cmdlet 會取得服務端點原則。</span><span class="sxs-lookup"><span data-stu-id="8dc78-108">The **Get-AzServiceEndpointPolicy** cmdlet gets a service endpoint policy.</span></span>

## <span data-ttu-id="8dc78-109">示例</span><span class="sxs-lookup"><span data-stu-id="8dc78-109">EXAMPLES</span></span>

### <span data-ttu-id="8dc78-110">範例1</span><span class="sxs-lookup"><span data-stu-id="8dc78-110">Example 1</span></span>
```
$policy = Get-AzServiceEndpointPolicy -Name "ServiceEndpointPolicy1" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="8dc78-111">這個命令會取得屬於名為 ResourceGroup01 之資源群組的名為 ServiceEndpointPolicy1 的服務端點原則，並將它儲存在 $policy 變數中。</span><span class="sxs-lookup"><span data-stu-id="8dc78-111">This command gets the service endpoint policy named ServiceEndpointPolicy1 that belongs to the resource group named ResourceGroup01 and stores it in the $policy variable.</span></span>

### <span data-ttu-id="8dc78-112">範例2</span><span class="sxs-lookup"><span data-stu-id="8dc78-112">Example 2</span></span>
```
$policyList = Get-AzServiceEndpointPolicy -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="8dc78-113">這個命令會在名為 ResourceGroup01 的資源群組中取得所有服務端點原則的清單，並將它儲存在 $policyList 變數中。</span><span class="sxs-lookup"><span data-stu-id="8dc78-113">This command gets a list of all the service endpoint policies in the resource group named ResourceGroup01 and stores it in the $policyList variable.</span></span>

### <span data-ttu-id="8dc78-114">範例3</span><span class="sxs-lookup"><span data-stu-id="8dc78-114">Example 3</span></span>
```
$policyList = Get-AzServiceEndpointPolicy -ResourceGroupName "ServiceEndpointPolicy*"
```

<span data-ttu-id="8dc78-115">這個命令會取得以 "ServiceEndpointPolicy" 開頭的所有服務端點原則的清單。</span><span class="sxs-lookup"><span data-stu-id="8dc78-115">This command gets a list of all the service endpoint policies that start with "ServiceEndpointPolicy".</span></span>

## <span data-ttu-id="8dc78-116">參數</span><span class="sxs-lookup"><span data-stu-id="8dc78-116">PARAMETERS</span></span>

### <span data-ttu-id="8dc78-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8dc78-117">-DefaultProfile</span></span>
<span data-ttu-id="8dc78-118">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="8dc78-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8dc78-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="8dc78-119">-Name</span></span>
<span data-ttu-id="8dc78-120">服務端點原則的名稱</span><span class="sxs-lookup"><span data-stu-id="8dc78-120">The name of the service endpoint policy</span></span>

```yaml
Type: System.String
Parameter Sets: ListParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="8dc78-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8dc78-121">-ResourceGroupName</span></span>
<span data-ttu-id="8dc78-122">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="8dc78-122">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="8dc78-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8dc78-123">-ResourceId</span></span>
<span data-ttu-id="8dc78-124">服務端點原則的識別碼。</span><span class="sxs-lookup"><span data-stu-id="8dc78-124">The ID of the service endpoint policy.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8dc78-125">-確認</span><span class="sxs-lookup"><span data-stu-id="8dc78-125">-Confirm</span></span>
<span data-ttu-id="8dc78-126">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="8dc78-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8dc78-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8dc78-127">-WhatIf</span></span>
<span data-ttu-id="8dc78-128">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="8dc78-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8dc78-129">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8dc78-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8dc78-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8dc78-130">CommonParameters</span></span>
<span data-ttu-id="8dc78-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8dc78-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8dc78-132">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="8dc78-132">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8dc78-133">輸入</span><span class="sxs-lookup"><span data-stu-id="8dc78-133">INPUTS</span></span>

### <span data-ttu-id="8dc78-134">System.object</span><span class="sxs-lookup"><span data-stu-id="8dc78-134">System.String</span></span>

## <span data-ttu-id="8dc78-135">輸出</span><span class="sxs-lookup"><span data-stu-id="8dc78-135">OUTPUTS</span></span>

### <span data-ttu-id="8dc78-136">PSServiceEndpointPolicy 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="8dc78-136">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="8dc78-137">筆記</span><span class="sxs-lookup"><span data-stu-id="8dc78-137">NOTES</span></span>

## <span data-ttu-id="8dc78-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="8dc78-138">RELATED LINKS</span></span>

[<span data-ttu-id="8dc78-139">新-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="8dc78-139">New-AzServiceEndpointPolicy</span></span>](./New-AzServiceEndpointPolicy.md)

[<span data-ttu-id="8dc78-140">移除-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="8dc78-140">Remove-AzServiceEndpointPolicy</span></span>](./Remove-AzServiceEndpointPolicy.md)

[<span data-ttu-id="8dc78-141">Set-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="8dc78-141">Set-AzServiceEndpointPolicy</span></span>](./Set-AzServiceEndpointPolicy.md)
