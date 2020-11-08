---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationsecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationSecurityGroup.md
ms.openlocfilehash: 562a2fbf02bd6389b28543f09ace1c59b2e9ed1c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94135552"
---
# <span data-ttu-id="aebbf-101">Remove-AzApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="aebbf-101">Remove-AzApplicationSecurityGroup</span></span>

## <span data-ttu-id="aebbf-102">摘要</span><span class="sxs-lookup"><span data-stu-id="aebbf-102">SYNOPSIS</span></span>
<span data-ttu-id="aebbf-103">移除應用程式安全性群組。</span><span class="sxs-lookup"><span data-stu-id="aebbf-103">Removes an application security group.</span></span>

## <span data-ttu-id="aebbf-104">句法</span><span class="sxs-lookup"><span data-stu-id="aebbf-104">SYNTAX</span></span>

```
Remove-AzApplicationSecurityGroup -ResourceGroupName <String> -Name <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aebbf-105">說明</span><span class="sxs-lookup"><span data-stu-id="aebbf-105">DESCRIPTION</span></span>
<span data-ttu-id="aebbf-106">**AzApplicationSecurityGroup** Cmdlet 會移除應用程式安全性群組。</span><span class="sxs-lookup"><span data-stu-id="aebbf-106">The **Remove-AzApplicationSecurityGroup** cmdlet removes an application security group.</span></span>

## <span data-ttu-id="aebbf-107">示例</span><span class="sxs-lookup"><span data-stu-id="aebbf-107">EXAMPLES</span></span>

### <span data-ttu-id="aebbf-108">範例1</span><span class="sxs-lookup"><span data-stu-id="aebbf-108">Example 1</span></span>
```
PS C:\>Remove-AzApplicationSecurityGroup -Name "MyApplicationSecurityGrouo" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="aebbf-109">這個命令會刪除名為 MyResourceGroup 的資源群組中名為 MyApplicationSecurityGrouo 的應用程式安全性群組。</span><span class="sxs-lookup"><span data-stu-id="aebbf-109">This command deletes an application security group named MyApplicationSecurityGrouo in the resource group named MyResourceGroup.</span></span>

## <span data-ttu-id="aebbf-110">參數</span><span class="sxs-lookup"><span data-stu-id="aebbf-110">PARAMETERS</span></span>

### <span data-ttu-id="aebbf-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="aebbf-111">-AsJob</span></span>
<span data-ttu-id="aebbf-112">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="aebbf-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="aebbf-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aebbf-113">-DefaultProfile</span></span>
<span data-ttu-id="aebbf-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="aebbf-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="aebbf-115">-Force</span><span class="sxs-lookup"><span data-stu-id="aebbf-115">-Force</span></span>
<span data-ttu-id="aebbf-116">如果您想要刪除資源，請不要要求確認</span><span class="sxs-lookup"><span data-stu-id="aebbf-116">Do not ask for confirmation if you want to delete resource</span></span>

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

### <span data-ttu-id="aebbf-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="aebbf-117">-Name</span></span>
<span data-ttu-id="aebbf-118">應用程式安全性群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="aebbf-118">The name of the application security group.</span></span>

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

### <span data-ttu-id="aebbf-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="aebbf-119">-PassThru</span></span>
<span data-ttu-id="aebbf-120">傳回代表您正在使用之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="aebbf-120">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="aebbf-121">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="aebbf-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="aebbf-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aebbf-122">-ResourceGroupName</span></span>
<span data-ttu-id="aebbf-123">應用程式安全性群組的資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="aebbf-123">The resource group name of the application security group.</span></span>

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

### <span data-ttu-id="aebbf-124">-確認</span><span class="sxs-lookup"><span data-stu-id="aebbf-124">-Confirm</span></span>
<span data-ttu-id="aebbf-125">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="aebbf-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aebbf-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aebbf-126">-WhatIf</span></span>
<span data-ttu-id="aebbf-127">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="aebbf-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aebbf-128">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="aebbf-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aebbf-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aebbf-129">CommonParameters</span></span>
<span data-ttu-id="aebbf-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="aebbf-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aebbf-131">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="aebbf-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aebbf-132">輸入</span><span class="sxs-lookup"><span data-stu-id="aebbf-132">INPUTS</span></span>

### <span data-ttu-id="aebbf-133">System.object</span><span class="sxs-lookup"><span data-stu-id="aebbf-133">System.String</span></span>

## <span data-ttu-id="aebbf-134">輸出</span><span class="sxs-lookup"><span data-stu-id="aebbf-134">OUTPUTS</span></span>

### <span data-ttu-id="aebbf-135">System.object</span><span class="sxs-lookup"><span data-stu-id="aebbf-135">System.Boolean</span></span>

## <span data-ttu-id="aebbf-136">筆記</span><span class="sxs-lookup"><span data-stu-id="aebbf-136">NOTES</span></span>

## <span data-ttu-id="aebbf-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="aebbf-137">RELATED LINKS</span></span>

[<span data-ttu-id="aebbf-138">新-AzApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="aebbf-138">New-AzApplicationSecurityGroup</span></span>](./New-AzApplicationSecurityGroup.md)

[<span data-ttu-id="aebbf-139">AzApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="aebbf-139">Get-AzApplicationSecurityGroup</span></span>](./Get-AzApplicationSecurityGroup.md)
