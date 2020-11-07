---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationsecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzApplicationSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzApplicationSecurityGroup.md
ms.openlocfilehash: 1bdad35adef15c15c77753c77533f35cfaf945ea
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93794187"
---
# <span data-ttu-id="03a7c-101">Remove-AzApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="03a7c-101">Remove-AzApplicationSecurityGroup</span></span>

## <span data-ttu-id="03a7c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="03a7c-102">SYNOPSIS</span></span>
<span data-ttu-id="03a7c-103">移除應用程式安全性群組。</span><span class="sxs-lookup"><span data-stu-id="03a7c-103">Removes an application security group.</span></span>

## <span data-ttu-id="03a7c-104">句法</span><span class="sxs-lookup"><span data-stu-id="03a7c-104">SYNTAX</span></span>

```
Remove-AzApplicationSecurityGroup -ResourceGroupName <String> -Name <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="03a7c-105">說明</span><span class="sxs-lookup"><span data-stu-id="03a7c-105">DESCRIPTION</span></span>
<span data-ttu-id="03a7c-106">**AzApplicationSecurityGroup** Cmdlet 會移除應用程式安全性群組。</span><span class="sxs-lookup"><span data-stu-id="03a7c-106">The **Remove-AzApplicationSecurityGroup** cmdlet removes an application security group.</span></span>

## <span data-ttu-id="03a7c-107">示例</span><span class="sxs-lookup"><span data-stu-id="03a7c-107">EXAMPLES</span></span>

### <span data-ttu-id="03a7c-108">範例1</span><span class="sxs-lookup"><span data-stu-id="03a7c-108">Example 1</span></span>
```
PS C:\>Remove-AzApplicationSecurityGroup -Name "MyApplicationSecurityGrouo" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="03a7c-109">這個命令會刪除名為 MyResourceGroup 的資源群組中名為 MyApplicationSecurityGrouo 的應用程式安全性群組。</span><span class="sxs-lookup"><span data-stu-id="03a7c-109">This command deletes an application security group named MyApplicationSecurityGrouo in the resource group named MyResourceGroup.</span></span>

## <span data-ttu-id="03a7c-110">參數</span><span class="sxs-lookup"><span data-stu-id="03a7c-110">PARAMETERS</span></span>

### <span data-ttu-id="03a7c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03a7c-111">-DefaultProfile</span></span>
<span data-ttu-id="03a7c-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="03a7c-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03a7c-113">-Force</span><span class="sxs-lookup"><span data-stu-id="03a7c-113">-Force</span></span>
<span data-ttu-id="03a7c-114">如果您想要刪除資源，請不要要求確認</span><span class="sxs-lookup"><span data-stu-id="03a7c-114">Do not ask for confirmation if you want to delete resource</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03a7c-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="03a7c-115">-Name</span></span>
<span data-ttu-id="03a7c-116">應用程式安全性群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="03a7c-116">The name of the application security group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="03a7c-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="03a7c-117">-PassThru</span></span>
<span data-ttu-id="03a7c-118">傳回代表您正在使用之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="03a7c-118">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="03a7c-119">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="03a7c-119">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03a7c-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="03a7c-120">-ResourceGroupName</span></span>
<span data-ttu-id="03a7c-121">應用程式安全性群組的資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="03a7c-121">The resource group name of the application security group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="03a7c-122">-確認</span><span class="sxs-lookup"><span data-stu-id="03a7c-122">-Confirm</span></span>
<span data-ttu-id="03a7c-123">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="03a7c-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03a7c-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="03a7c-124">-WhatIf</span></span>
<span data-ttu-id="03a7c-125">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="03a7c-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="03a7c-126">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="03a7c-126">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03a7c-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03a7c-127">CommonParameters</span></span>
<span data-ttu-id="03a7c-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="03a7c-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03a7c-129">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="03a7c-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03a7c-130">輸入</span><span class="sxs-lookup"><span data-stu-id="03a7c-130">INPUTS</span></span>

### <span data-ttu-id="03a7c-131">System.object</span><span class="sxs-lookup"><span data-stu-id="03a7c-131">System.String</span></span>

## <span data-ttu-id="03a7c-132">輸出</span><span class="sxs-lookup"><span data-stu-id="03a7c-132">OUTPUTS</span></span>

### <span data-ttu-id="03a7c-133">System.object</span><span class="sxs-lookup"><span data-stu-id="03a7c-133">System.Object</span></span>

## <span data-ttu-id="03a7c-134">筆記</span><span class="sxs-lookup"><span data-stu-id="03a7c-134">NOTES</span></span>

## <span data-ttu-id="03a7c-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="03a7c-135">RELATED LINKS</span></span>

[<span data-ttu-id="03a7c-136">新-AzApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="03a7c-136">New-AzApplicationSecurityGroup</span></span>](./New-AzApplicationSecurityGroup.md)

[<span data-ttu-id="03a7c-137">AzApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="03a7c-137">Get-AzApplicationSecurityGroup</span></span>](./Get-AzApplicationSecurityGroup.md)
