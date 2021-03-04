---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: E9390015-FD5C-4015-BA81-3445ADF8F8BF
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azapplicationgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGateway.md
ms.openlocfilehash: 7095190570e649ab5262de0a8cebfc97d55fbf17
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101909997"
---
# <span data-ttu-id="8b004-101">Remove-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8b004-101">Remove-AzApplicationGateway</span></span>

## <span data-ttu-id="8b004-102">簡介</span><span class="sxs-lookup"><span data-stu-id="8b004-102">SYNOPSIS</span></span>
<span data-ttu-id="8b004-103">移除應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="8b004-103">Removes an application gateway.</span></span>

## <span data-ttu-id="8b004-104">語法</span><span class="sxs-lookup"><span data-stu-id="8b004-104">SYNTAX</span></span>

```
Remove-AzApplicationGateway -Name <String> -ResourceGroupName <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8b004-105">描述</span><span class="sxs-lookup"><span data-stu-id="8b004-105">DESCRIPTION</span></span>
<span data-ttu-id="8b004-106">**Remove-AzApplicationGateway** Cmdlet 會移除應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="8b004-106">The **Remove-AzApplicationGateway** cmdlet removes an application gateway.</span></span>

## <span data-ttu-id="8b004-107">例子</span><span class="sxs-lookup"><span data-stu-id="8b004-107">EXAMPLES</span></span>

### <span data-ttu-id="8b004-108">範例 1：移除指定的應用程式閘道</span><span class="sxs-lookup"><span data-stu-id="8b004-108">Example 1: Remove a specified application gateway</span></span>
```
PS C:\>Remove-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="8b004-109">此命令會移除名為 ResourceGroup01 的資源群組中名為 ApplicationGateway01 的應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="8b004-109">This command removes the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="8b004-110">參數</span><span class="sxs-lookup"><span data-stu-id="8b004-110">PARAMETERS</span></span>

### <span data-ttu-id="8b004-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b004-111">-DefaultProfile</span></span>
<span data-ttu-id="8b004-112">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="8b004-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8b004-113">-強制</span><span class="sxs-lookup"><span data-stu-id="8b004-113">-Force</span></span>
<span data-ttu-id="8b004-114">表示不論是否指派資源給 Cmdlet，都會強制刪除應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="8b004-114">Indicates that the cmdlet forces the deletion of the application gateway regardless of whether resources are assigned to it.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8b004-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="8b004-115">-Name</span></span>
<span data-ttu-id="8b004-116">指定要移除的應用程式閘道名稱。</span><span class="sxs-lookup"><span data-stu-id="8b004-116">Specifies the name of the application gateway to be removed.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8b004-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8b004-117">-PassThru</span></span>
<span data-ttu-id="8b004-118">會返回代表您處理之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="8b004-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="8b004-119">根據預設，此 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="8b004-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="8b004-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8b004-120">-ResourceGroupName</span></span>
<span data-ttu-id="8b004-121">指定應用程式閘道所屬的資源組名。</span><span class="sxs-lookup"><span data-stu-id="8b004-121">Specifies the name of the resource group name that the application gateway belongs to.</span></span>

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

### <span data-ttu-id="8b004-122">-確認</span><span class="sxs-lookup"><span data-stu-id="8b004-122">-Confirm</span></span>
<span data-ttu-id="8b004-123">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="8b004-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b004-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8b004-124">-WhatIf</span></span>
<span data-ttu-id="8b004-125">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="8b004-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8b004-126">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8b004-126">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b004-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b004-127">CommonParameters</span></span>
<span data-ttu-id="8b004-128">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="8b004-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b004-129">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="8b004-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b004-130">輸入</span><span class="sxs-lookup"><span data-stu-id="8b004-130">INPUTS</span></span>

### <span data-ttu-id="8b004-131">System.String</span><span class="sxs-lookup"><span data-stu-id="8b004-131">System.String</span></span>

### <span data-ttu-id="8b004-132">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="8b004-132">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="8b004-133">輸出</span><span class="sxs-lookup"><span data-stu-id="8b004-133">OUTPUTS</span></span>

### <span data-ttu-id="8b004-134">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="8b004-134">System.Boolean</span></span>

## <span data-ttu-id="8b004-135">筆記</span><span class="sxs-lookup"><span data-stu-id="8b004-135">NOTES</span></span>

## <span data-ttu-id="8b004-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="8b004-136">RELATED LINKS</span></span>

[<span data-ttu-id="8b004-137">Set-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8b004-137">Set-AzApplicationGateway</span></span>](./Set-AzApplicationGateway.md)


