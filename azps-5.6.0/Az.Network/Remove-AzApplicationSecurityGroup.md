---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azapplicationsecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationSecurityGroup.md
ms.openlocfilehash: 72b7fa033696fb5daba364a45713294a8b54831b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101903994"
---
# <span data-ttu-id="8d033-101">Remove-AzApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="8d033-101">Remove-AzApplicationSecurityGroup</span></span>

## <span data-ttu-id="8d033-102">簡介</span><span class="sxs-lookup"><span data-stu-id="8d033-102">SYNOPSIS</span></span>
<span data-ttu-id="8d033-103">移除應用程式安全性群組。</span><span class="sxs-lookup"><span data-stu-id="8d033-103">Removes an application security group.</span></span>

## <span data-ttu-id="8d033-104">語法</span><span class="sxs-lookup"><span data-stu-id="8d033-104">SYNTAX</span></span>

```
Remove-AzApplicationSecurityGroup -ResourceGroupName <String> -Name <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8d033-105">描述</span><span class="sxs-lookup"><span data-stu-id="8d033-105">DESCRIPTION</span></span>
<span data-ttu-id="8d033-106">**Remove-AzApplicationSecurityGroup** Cmdlet 會移除應用程式安全性群組。</span><span class="sxs-lookup"><span data-stu-id="8d033-106">The **Remove-AzApplicationSecurityGroup** cmdlet removes an application security group.</span></span>

## <span data-ttu-id="8d033-107">例子</span><span class="sxs-lookup"><span data-stu-id="8d033-107">EXAMPLES</span></span>

### <span data-ttu-id="8d033-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="8d033-108">Example 1</span></span>
```
PS C:\>Remove-AzApplicationSecurityGroup -Name "MyApplicationSecurityGrouo" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="8d033-109">此命令會刪除名為 MyResourceGroup 的資源群組中名為 MyApplicationSecurityGro一的應用程式安全性群組。</span><span class="sxs-lookup"><span data-stu-id="8d033-109">This command deletes an application security group named MyApplicationSecurityGrouo in the resource group named MyResourceGroup.</span></span>

## <span data-ttu-id="8d033-110">參數</span><span class="sxs-lookup"><span data-stu-id="8d033-110">PARAMETERS</span></span>

### <span data-ttu-id="8d033-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8d033-111">-AsJob</span></span>
<span data-ttu-id="8d033-112">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="8d033-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8d033-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d033-113">-DefaultProfile</span></span>
<span data-ttu-id="8d033-114">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="8d033-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8d033-115">-強制</span><span class="sxs-lookup"><span data-stu-id="8d033-115">-Force</span></span>
<span data-ttu-id="8d033-116">如果您要刪除資源，請勿要求確認</span><span class="sxs-lookup"><span data-stu-id="8d033-116">Do not ask for confirmation if you want to delete resource</span></span>

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

### <span data-ttu-id="8d033-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="8d033-117">-Name</span></span>
<span data-ttu-id="8d033-118">應用程式安全性群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="8d033-118">The name of the application security group.</span></span>

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

### <span data-ttu-id="8d033-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8d033-119">-PassThru</span></span>
<span data-ttu-id="8d033-120">會返回代表您處理之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="8d033-120">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="8d033-121">根據預設，此 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="8d033-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="8d033-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8d033-122">-ResourceGroupName</span></span>
<span data-ttu-id="8d033-123">應用程式安全性群組的資源組名。</span><span class="sxs-lookup"><span data-stu-id="8d033-123">The resource group name of the application security group.</span></span>

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

### <span data-ttu-id="8d033-124">-確認</span><span class="sxs-lookup"><span data-stu-id="8d033-124">-Confirm</span></span>
<span data-ttu-id="8d033-125">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="8d033-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8d033-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8d033-126">-WhatIf</span></span>
<span data-ttu-id="8d033-127">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="8d033-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8d033-128">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8d033-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8d033-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d033-129">CommonParameters</span></span>
<span data-ttu-id="8d033-130">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="8d033-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d033-131">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="8d033-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d033-132">輸入</span><span class="sxs-lookup"><span data-stu-id="8d033-132">INPUTS</span></span>

### <span data-ttu-id="8d033-133">System.String</span><span class="sxs-lookup"><span data-stu-id="8d033-133">System.String</span></span>

## <span data-ttu-id="8d033-134">輸出</span><span class="sxs-lookup"><span data-stu-id="8d033-134">OUTPUTS</span></span>

### <span data-ttu-id="8d033-135">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="8d033-135">System.Boolean</span></span>

## <span data-ttu-id="8d033-136">筆記</span><span class="sxs-lookup"><span data-stu-id="8d033-136">NOTES</span></span>

## <span data-ttu-id="8d033-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="8d033-137">RELATED LINKS</span></span>

[<span data-ttu-id="8d033-138">New-AzApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="8d033-138">New-AzApplicationSecurityGroup</span></span>](./New-AzApplicationSecurityGroup.md)

[<span data-ttu-id="8d033-139">Get-AzApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="8d033-139">Get-AzApplicationSecurityGroup</span></span>](./Get-AzApplicationSecurityGroup.md)
