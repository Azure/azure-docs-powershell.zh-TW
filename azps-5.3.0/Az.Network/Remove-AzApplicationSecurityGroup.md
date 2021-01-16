---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationsecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationSecurityGroup.md
ms.openlocfilehash: 562a2fbf02bd6389b28543f09ace1c59b2e9ed1c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98288679"
---
# <span data-ttu-id="fe4a2-101">Remove-AzApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="fe4a2-101">Remove-AzApplicationSecurityGroup</span></span>

## <span data-ttu-id="fe4a2-102">摘要</span><span class="sxs-lookup"><span data-stu-id="fe4a2-102">SYNOPSIS</span></span>
<span data-ttu-id="fe4a2-103">移除應用程式安全性群組。</span><span class="sxs-lookup"><span data-stu-id="fe4a2-103">Removes an application security group.</span></span>

## <span data-ttu-id="fe4a2-104">句法</span><span class="sxs-lookup"><span data-stu-id="fe4a2-104">SYNTAX</span></span>

```
Remove-AzApplicationSecurityGroup -ResourceGroupName <String> -Name <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fe4a2-105">說明</span><span class="sxs-lookup"><span data-stu-id="fe4a2-105">DESCRIPTION</span></span>
<span data-ttu-id="fe4a2-106">**AzApplicationSecurityGroup** Cmdlet 會移除應用程式安全性群組。</span><span class="sxs-lookup"><span data-stu-id="fe4a2-106">The **Remove-AzApplicationSecurityGroup** cmdlet removes an application security group.</span></span>

## <span data-ttu-id="fe4a2-107">示例</span><span class="sxs-lookup"><span data-stu-id="fe4a2-107">EXAMPLES</span></span>

### <span data-ttu-id="fe4a2-108">範例1</span><span class="sxs-lookup"><span data-stu-id="fe4a2-108">Example 1</span></span>
```
PS C:\>Remove-AzApplicationSecurityGroup -Name "MyApplicationSecurityGrouo" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="fe4a2-109">這個命令會刪除名為 MyResourceGroup 的資源群組中名為 MyApplicationSecurityGrouo 的應用程式安全性群組。</span><span class="sxs-lookup"><span data-stu-id="fe4a2-109">This command deletes an application security group named MyApplicationSecurityGrouo in the resource group named MyResourceGroup.</span></span>

## <span data-ttu-id="fe4a2-110">參數</span><span class="sxs-lookup"><span data-stu-id="fe4a2-110">PARAMETERS</span></span>

### <span data-ttu-id="fe4a2-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fe4a2-111">-AsJob</span></span>
<span data-ttu-id="fe4a2-112">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="fe4a2-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="fe4a2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe4a2-113">-DefaultProfile</span></span>
<span data-ttu-id="fe4a2-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="fe4a2-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fe4a2-115">-Force</span><span class="sxs-lookup"><span data-stu-id="fe4a2-115">-Force</span></span>
<span data-ttu-id="fe4a2-116">如果您想要刪除資源，請不要要求確認</span><span class="sxs-lookup"><span data-stu-id="fe4a2-116">Do not ask for confirmation if you want to delete resource</span></span>

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

### <span data-ttu-id="fe4a2-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="fe4a2-117">-Name</span></span>
<span data-ttu-id="fe4a2-118">應用程式安全性群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="fe4a2-118">The name of the application security group.</span></span>

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

### <span data-ttu-id="fe4a2-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fe4a2-119">-PassThru</span></span>
<span data-ttu-id="fe4a2-120">傳回代表您正在使用之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="fe4a2-120">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="fe4a2-121">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="fe4a2-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="fe4a2-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fe4a2-122">-ResourceGroupName</span></span>
<span data-ttu-id="fe4a2-123">應用程式安全性群組的資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="fe4a2-123">The resource group name of the application security group.</span></span>

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

### <span data-ttu-id="fe4a2-124">-確認</span><span class="sxs-lookup"><span data-stu-id="fe4a2-124">-Confirm</span></span>
<span data-ttu-id="fe4a2-125">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="fe4a2-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fe4a2-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fe4a2-126">-WhatIf</span></span>
<span data-ttu-id="fe4a2-127">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="fe4a2-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fe4a2-128">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="fe4a2-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fe4a2-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe4a2-129">CommonParameters</span></span>
<span data-ttu-id="fe4a2-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="fe4a2-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe4a2-131">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="fe4a2-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe4a2-132">輸入</span><span class="sxs-lookup"><span data-stu-id="fe4a2-132">INPUTS</span></span>

### <span data-ttu-id="fe4a2-133">System.object</span><span class="sxs-lookup"><span data-stu-id="fe4a2-133">System.String</span></span>

## <span data-ttu-id="fe4a2-134">輸出</span><span class="sxs-lookup"><span data-stu-id="fe4a2-134">OUTPUTS</span></span>

### <span data-ttu-id="fe4a2-135">System.object</span><span class="sxs-lookup"><span data-stu-id="fe4a2-135">System.Boolean</span></span>

## <span data-ttu-id="fe4a2-136">筆記</span><span class="sxs-lookup"><span data-stu-id="fe4a2-136">NOTES</span></span>

## <span data-ttu-id="fe4a2-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="fe4a2-137">RELATED LINKS</span></span>

[<span data-ttu-id="fe4a2-138">新-AzApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="fe4a2-138">New-AzApplicationSecurityGroup</span></span>](./New-AzApplicationSecurityGroup.md)

[<span data-ttu-id="fe4a2-139">AzApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="fe4a2-139">Get-AzApplicationSecurityGroup</span></span>](./Get-AzApplicationSecurityGroup.md)
