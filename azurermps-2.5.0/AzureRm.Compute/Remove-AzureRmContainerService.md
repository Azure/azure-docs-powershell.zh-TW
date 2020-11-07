---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 8180092D-5B1D-43A0-B830-D009B30E2DDF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermcontainerservice
schema: 2.0.0
ms.openlocfilehash: 27d1e45a9e2c85fb3d2f7470db97ce2426f62a19
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93801742"
---
# <span data-ttu-id="00478-101">Remove-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="00478-101">Remove-AzureRmContainerService</span></span>

## <span data-ttu-id="00478-102">摘要</span><span class="sxs-lookup"><span data-stu-id="00478-102">SYNOPSIS</span></span>
<span data-ttu-id="00478-103">移除容器服務。</span><span class="sxs-lookup"><span data-stu-id="00478-103">Removes a container service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="00478-104">句法</span><span class="sxs-lookup"><span data-stu-id="00478-104">SYNTAX</span></span>

```
Remove-AzureRmContainerService [-ResourceGroupName] <String> [-Name] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="00478-105">說明</span><span class="sxs-lookup"><span data-stu-id="00478-105">DESCRIPTION</span></span>
<span data-ttu-id="00478-106">**AzureRmContainerService** Cmdlet 會從您的 Azure 帳戶中移除容器服務。</span><span class="sxs-lookup"><span data-stu-id="00478-106">The **Remove-AzureRmContainerService** cmdlet removes a container service from your Azure account.</span></span>

## <span data-ttu-id="00478-107">示例</span><span class="sxs-lookup"><span data-stu-id="00478-107">EXAMPLES</span></span>

### <span data-ttu-id="00478-108">範例1：移除容器服務</span><span class="sxs-lookup"><span data-stu-id="00478-108">Example 1: Remove a container service</span></span>
```
PS C:\> Remove-AzureRmContainerService -ResourceGroupName "ResourceGroup17" -Name "CSResourceGroup17"
```

<span data-ttu-id="00478-109">這個命令會移除名為 CSResourceGroup17 的容器服務。</span><span class="sxs-lookup"><span data-stu-id="00478-109">This command removes the container service named CSResourceGroup17.</span></span>

## <span data-ttu-id="00478-110">參數</span><span class="sxs-lookup"><span data-stu-id="00478-110">PARAMETERS</span></span>

### <span data-ttu-id="00478-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="00478-111">-AsJob</span></span>
<span data-ttu-id="00478-112">在背景中執行 Cmdlet，然後返回作業來追蹤進度。</span><span class="sxs-lookup"><span data-stu-id="00478-112">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="00478-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="00478-113">-DefaultProfile</span></span>
<span data-ttu-id="00478-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="00478-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="00478-115">-Force</span><span class="sxs-lookup"><span data-stu-id="00478-115">-Force</span></span>
<span data-ttu-id="00478-116">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="00478-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="00478-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="00478-117">-Name</span></span>
<span data-ttu-id="00478-118">指定此 Cmdlet 移除的容器服務名稱。</span><span class="sxs-lookup"><span data-stu-id="00478-118">Specifies the name of the container service that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="00478-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="00478-119">-ResourceGroupName</span></span>
<span data-ttu-id="00478-120">指定此 Cmdlet 移除之容器服務的 [資源] 群組。</span><span class="sxs-lookup"><span data-stu-id="00478-120">Specifies the resource group of the container service that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="00478-121">-確認</span><span class="sxs-lookup"><span data-stu-id="00478-121">-Confirm</span></span>
<span data-ttu-id="00478-122">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="00478-122">Prompts you for confirmation before running the cmdlet.</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00478-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="00478-123">-WhatIf</span></span>
<span data-ttu-id="00478-124">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="00478-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="00478-125">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="00478-125">The cmdlet is not run.</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00478-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00478-126">CommonParameters</span></span>
<span data-ttu-id="00478-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="00478-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00478-128">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="00478-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00478-129">輸入</span><span class="sxs-lookup"><span data-stu-id="00478-129">INPUTS</span></span>

### <span data-ttu-id="00478-130">所有</span><span class="sxs-lookup"><span data-stu-id="00478-130">None</span></span>
<span data-ttu-id="00478-131">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="00478-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="00478-132">輸出</span><span class="sxs-lookup"><span data-stu-id="00478-132">OUTPUTS</span></span>

### <span data-ttu-id="00478-133">System.void</span><span class="sxs-lookup"><span data-stu-id="00478-133">System.Void</span></span>

## <span data-ttu-id="00478-134">筆記</span><span class="sxs-lookup"><span data-stu-id="00478-134">NOTES</span></span>

## <span data-ttu-id="00478-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="00478-135">RELATED LINKS</span></span>

[<span data-ttu-id="00478-136">AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="00478-136">Get-AzureRmContainerService</span></span>](./Get-AzureRmContainerService.md)

[<span data-ttu-id="00478-137">新-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="00478-137">New-AzureRmContainerService</span></span>](./New-AzureRmContainerService.md)

[<span data-ttu-id="00478-138">更新-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="00478-138">Update-AzureRmContainerService</span></span>](./Update-AzureRmContainerService.md)


