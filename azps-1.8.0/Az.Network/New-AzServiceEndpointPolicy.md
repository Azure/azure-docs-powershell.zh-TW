---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azserviceendpointpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzServiceEndpointPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzServiceEndpointPolicy.md
ms.openlocfilehash: e7025a48fd1d83a0018ac18de01673b0deeed742
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93621723"
---
# <span data-ttu-id="3e07a-101">New-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="3e07a-101">New-AzServiceEndpointPolicy</span></span>

## <span data-ttu-id="3e07a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="3e07a-102">SYNOPSIS</span></span>
<span data-ttu-id="3e07a-103">建立服務端點原則。</span><span class="sxs-lookup"><span data-stu-id="3e07a-103">Creates a service endpoint policy.</span></span>

## <span data-ttu-id="3e07a-104">句法</span><span class="sxs-lookup"><span data-stu-id="3e07a-104">SYNTAX</span></span>

```
New-AzServiceEndpointPolicy -Name <String>
 [-ServiceEndpointPolicyDefinition <PSServiceEndpointPolicyDefinition[]>] -ResourceGroupName <String>
 -Location <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3e07a-105">說明</span><span class="sxs-lookup"><span data-stu-id="3e07a-105">DESCRIPTION</span></span>
<span data-ttu-id="3e07a-106">**新的-AzServiceEndpointPolicy** Cmdlet 會建立服務端點原則。</span><span class="sxs-lookup"><span data-stu-id="3e07a-106">The **New-AzServiceEndpointPolicy** cmdlet create a service endpoint policy.</span></span>

## <span data-ttu-id="3e07a-107">示例</span><span class="sxs-lookup"><span data-stu-id="3e07a-107">EXAMPLES</span></span>

### <span data-ttu-id="3e07a-108">範例1：建立服務端點原則</span><span class="sxs-lookup"><span data-stu-id="3e07a-108">Example 1: Creates a service endpoint policy</span></span>
```
$serviceEndpointPolicy = New-AzServiceEndpointPolicy -Name "Policy1" -ServiceEndpointPolicyDefinition $serviceEndpointDefinition -Location "location";
```

<span data-ttu-id="3e07a-109">這個命令會建立名為 Policy1 的服務端點原則，其中定義由 $serviceEndpointDefinition 物件定義的定義，並將其儲存在 $serviceEndpointPolicy 變數中。</span><span class="sxs-lookup"><span data-stu-id="3e07a-109">This command creates a service endpoint policy named Policy1 with definitions defined by the object $serviceEndpointDefinition and stores it in the $serviceEndpointPolicy variable.</span></span>

## <span data-ttu-id="3e07a-110">參數</span><span class="sxs-lookup"><span data-stu-id="3e07a-110">PARAMETERS</span></span>

### <span data-ttu-id="3e07a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e07a-111">-DefaultProfile</span></span>
<span data-ttu-id="3e07a-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="3e07a-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3e07a-113">-Force</span><span class="sxs-lookup"><span data-stu-id="3e07a-113">-Force</span></span>
<span data-ttu-id="3e07a-114">如果您想要 overrite 資源，請不要要求確認</span><span class="sxs-lookup"><span data-stu-id="3e07a-114">Do not ask for confirmation if you want to overrite a resource</span></span>

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

### <span data-ttu-id="3e07a-115">-位置</span><span class="sxs-lookup"><span data-stu-id="3e07a-115">-Location</span></span>
<span data-ttu-id="3e07a-116">位於.</span><span class="sxs-lookup"><span data-stu-id="3e07a-116">location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3e07a-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="3e07a-117">-Name</span></span>
<span data-ttu-id="3e07a-118">子網的名稱</span><span class="sxs-lookup"><span data-stu-id="3e07a-118">The name of the subnet</span></span>

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

### <span data-ttu-id="3e07a-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3e07a-119">-ResourceGroupName</span></span>
<span data-ttu-id="3e07a-120">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="3e07a-120">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3e07a-121">-ServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="3e07a-121">-ServiceEndpointPolicyDefinition</span></span>
<span data-ttu-id="3e07a-122">服務端點定義清單</span><span class="sxs-lookup"><span data-stu-id="3e07a-122">List of service endpoint definitions</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicyDefinition[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e07a-123">-確認</span><span class="sxs-lookup"><span data-stu-id="3e07a-123">-Confirm</span></span>
<span data-ttu-id="3e07a-124">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="3e07a-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3e07a-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3e07a-125">-WhatIf</span></span>
<span data-ttu-id="3e07a-126">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="3e07a-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3e07a-127">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="3e07a-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3e07a-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e07a-128">CommonParameters</span></span>
<span data-ttu-id="3e07a-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="3e07a-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e07a-130">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="3e07a-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e07a-131">輸入</span><span class="sxs-lookup"><span data-stu-id="3e07a-131">INPUTS</span></span>

### <span data-ttu-id="3e07a-132">System.object</span><span class="sxs-lookup"><span data-stu-id="3e07a-132">System.String</span></span>

## <span data-ttu-id="3e07a-133">輸出</span><span class="sxs-lookup"><span data-stu-id="3e07a-133">OUTPUTS</span></span>

### <span data-ttu-id="3e07a-134">PSServiceEndpointPolicy 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="3e07a-134">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="3e07a-135">筆記</span><span class="sxs-lookup"><span data-stu-id="3e07a-135">NOTES</span></span>

## <span data-ttu-id="3e07a-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="3e07a-136">RELATED LINKS</span></span>

[<span data-ttu-id="3e07a-137">AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="3e07a-137">Get-AzServiceEndpointPolicy</span></span>](./Get-AzServiceEndpointPolicy.md)

[<span data-ttu-id="3e07a-138">移除-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="3e07a-138">Remove-AzServiceEndpointPolicy</span></span>](./Remove-AzServiceEndpointPolicy.md)

[<span data-ttu-id="3e07a-139">Set-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="3e07a-139">Set-AzServiceEndpointPolicy</span></span>](./Set-AzServiceEndpointPolicy.md)
