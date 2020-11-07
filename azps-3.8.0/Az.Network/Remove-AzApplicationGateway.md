---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: E9390015-FD5C-4015-BA81-3445ADF8F8BF
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGateway.md
ms.openlocfilehash: aa8c40d7fb9f5ccb99ccdd88d6c04ceb4a888bf2
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93965768"
---
# <span data-ttu-id="81d50-101">Remove-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="81d50-101">Remove-AzApplicationGateway</span></span>

## <span data-ttu-id="81d50-102">摘要</span><span class="sxs-lookup"><span data-stu-id="81d50-102">SYNOPSIS</span></span>
<span data-ttu-id="81d50-103">移除應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="81d50-103">Removes an application gateway.</span></span>

## <span data-ttu-id="81d50-104">句法</span><span class="sxs-lookup"><span data-stu-id="81d50-104">SYNTAX</span></span>

```
Remove-AzApplicationGateway -Name <String> -ResourceGroupName <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="81d50-105">說明</span><span class="sxs-lookup"><span data-stu-id="81d50-105">DESCRIPTION</span></span>
<span data-ttu-id="81d50-106">**AzApplicationGateway** Cmdlet 會移除應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="81d50-106">The **Remove-AzApplicationGateway** cmdlet removes an application gateway.</span></span>

## <span data-ttu-id="81d50-107">示例</span><span class="sxs-lookup"><span data-stu-id="81d50-107">EXAMPLES</span></span>

### <span data-ttu-id="81d50-108">範例1：移除指定的應用程式閘道</span><span class="sxs-lookup"><span data-stu-id="81d50-108">Example 1: Remove a specified application gateway</span></span>
```
PS C:\>Remove-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="81d50-109">這個命令會移除名為 ResourceGroup01 的資源群組中名為 ApplicationGateway01 的應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="81d50-109">This command removes the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="81d50-110">參數</span><span class="sxs-lookup"><span data-stu-id="81d50-110">PARAMETERS</span></span>

### <span data-ttu-id="81d50-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81d50-111">-DefaultProfile</span></span>
<span data-ttu-id="81d50-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="81d50-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="81d50-113">-Force</span><span class="sxs-lookup"><span data-stu-id="81d50-113">-Force</span></span>
<span data-ttu-id="81d50-114">表示無論是否指派資源，該 Cmdlet 都會強制刪除應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="81d50-114">Indicates that the cmdlet forces the deletion of the application gateway regardless of whether resources are assigned to it.</span></span>

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

### <span data-ttu-id="81d50-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="81d50-115">-Name</span></span>
<span data-ttu-id="81d50-116">指定要移除之應用程式閘道的名稱。</span><span class="sxs-lookup"><span data-stu-id="81d50-116">Specifies the name of the application gateway to be removed.</span></span>

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

### <span data-ttu-id="81d50-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="81d50-117">-PassThru</span></span>
<span data-ttu-id="81d50-118">傳回代表您正在使用之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="81d50-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="81d50-119">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="81d50-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="81d50-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="81d50-120">-ResourceGroupName</span></span>
<span data-ttu-id="81d50-121">指定應用程式閘道所屬之資源組名稱的名稱。</span><span class="sxs-lookup"><span data-stu-id="81d50-121">Specifies the name of the resource group name that the application gateway belongs to.</span></span>

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

### <span data-ttu-id="81d50-122">-確認</span><span class="sxs-lookup"><span data-stu-id="81d50-122">-Confirm</span></span>
<span data-ttu-id="81d50-123">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="81d50-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="81d50-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="81d50-124">-WhatIf</span></span>
<span data-ttu-id="81d50-125">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="81d50-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="81d50-126">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="81d50-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="81d50-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81d50-127">CommonParameters</span></span>
<span data-ttu-id="81d50-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="81d50-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81d50-129">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="81d50-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81d50-130">輸入</span><span class="sxs-lookup"><span data-stu-id="81d50-130">INPUTS</span></span>

### <span data-ttu-id="81d50-131">System.object</span><span class="sxs-lookup"><span data-stu-id="81d50-131">System.String</span></span>

### <span data-ttu-id="81d50-132">SwitchParameter 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="81d50-132">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="81d50-133">輸出</span><span class="sxs-lookup"><span data-stu-id="81d50-133">OUTPUTS</span></span>

### <span data-ttu-id="81d50-134">System.object</span><span class="sxs-lookup"><span data-stu-id="81d50-134">System.Boolean</span></span>

## <span data-ttu-id="81d50-135">筆記</span><span class="sxs-lookup"><span data-stu-id="81d50-135">NOTES</span></span>

## <span data-ttu-id="81d50-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="81d50-136">RELATED LINKS</span></span>

[<span data-ttu-id="81d50-137">Set-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="81d50-137">Set-AzApplicationGateway</span></span>](./Set-AzApplicationGateway.md)


