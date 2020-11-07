---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 8180092D-5B1D-43A0-B830-D009B30E2DDF
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmContainerService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmContainerService.md
ms.openlocfilehash: fc66151f39c969ebbdc9b54d6f6ed97db909e05b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93626013"
---
# <span data-ttu-id="861bf-101">Remove-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="861bf-101">Remove-AzureRmContainerService</span></span>

## <span data-ttu-id="861bf-102">摘要</span><span class="sxs-lookup"><span data-stu-id="861bf-102">SYNOPSIS</span></span>
<span data-ttu-id="861bf-103">移除容器服務。</span><span class="sxs-lookup"><span data-stu-id="861bf-103">Removes a container service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="861bf-104">句法</span><span class="sxs-lookup"><span data-stu-id="861bf-104">SYNTAX</span></span>

```
Remove-AzureRmContainerService [-ResourceGroupName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="861bf-105">說明</span><span class="sxs-lookup"><span data-stu-id="861bf-105">DESCRIPTION</span></span>
<span data-ttu-id="861bf-106">**AzureRmContainerService** Cmdlet 會從您的 Azure 帳戶中移除容器服務。</span><span class="sxs-lookup"><span data-stu-id="861bf-106">The **Remove-AzureRmContainerService** cmdlet removes a container service from your Azure account.</span></span>

## <span data-ttu-id="861bf-107">示例</span><span class="sxs-lookup"><span data-stu-id="861bf-107">EXAMPLES</span></span>

### <span data-ttu-id="861bf-108">範例1：移除容器服務</span><span class="sxs-lookup"><span data-stu-id="861bf-108">Example 1: Remove a container service</span></span>
```
PS C:\> Remove-AzureRmContainerService -ResourceGroupName "ResourceGroup17" -Name "CSResourceGroup17"
```

<span data-ttu-id="861bf-109">這個命令會移除名為 CSResourceGroup17 的容器服務。</span><span class="sxs-lookup"><span data-stu-id="861bf-109">This command removes the container service named CSResourceGroup17.</span></span>

## <span data-ttu-id="861bf-110">參數</span><span class="sxs-lookup"><span data-stu-id="861bf-110">PARAMETERS</span></span>

### <span data-ttu-id="861bf-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="861bf-111">-DefaultProfile</span></span>
<span data-ttu-id="861bf-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="861bf-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="861bf-113">-Force</span><span class="sxs-lookup"><span data-stu-id="861bf-113">-Force</span></span>
<span data-ttu-id="861bf-114">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="861bf-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="861bf-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="861bf-115">-Name</span></span>
<span data-ttu-id="861bf-116">指定此 Cmdlet 移除的容器服務名稱。</span><span class="sxs-lookup"><span data-stu-id="861bf-116">Specifies the name of the container service that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="861bf-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="861bf-117">-ResourceGroupName</span></span>
<span data-ttu-id="861bf-118">指定此 Cmdlet 移除之容器服務的 [資源] 群組。</span><span class="sxs-lookup"><span data-stu-id="861bf-118">Specifies the resource group of the container service that this cmdlet removes.</span></span>

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

### <span data-ttu-id="861bf-119">-確認</span><span class="sxs-lookup"><span data-stu-id="861bf-119">-Confirm</span></span>
<span data-ttu-id="861bf-120">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="861bf-120">Prompts you for confirmation before running the cmdlet.</span></span>
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

### <span data-ttu-id="861bf-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="861bf-121">-WhatIf</span></span>
<span data-ttu-id="861bf-122">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="861bf-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="861bf-123">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="861bf-123">The cmdlet is not run.</span></span>
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

### <span data-ttu-id="861bf-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="861bf-124">CommonParameters</span></span>
<span data-ttu-id="861bf-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="861bf-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="861bf-126">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="861bf-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="861bf-127">輸入</span><span class="sxs-lookup"><span data-stu-id="861bf-127">INPUTS</span></span>

## <span data-ttu-id="861bf-128">輸出</span><span class="sxs-lookup"><span data-stu-id="861bf-128">OUTPUTS</span></span>

## <span data-ttu-id="861bf-129">筆記</span><span class="sxs-lookup"><span data-stu-id="861bf-129">NOTES</span></span>

## <span data-ttu-id="861bf-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="861bf-130">RELATED LINKS</span></span>

[<span data-ttu-id="861bf-131">AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="861bf-131">Get-AzureRmContainerService</span></span>](./Get-AzureRmContainerService.md)

[<span data-ttu-id="861bf-132">新-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="861bf-132">New-AzureRmContainerService</span></span>](./New-AzureRmContainerService.md)

[<span data-ttu-id="861bf-133">更新-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="861bf-133">Update-AzureRmContainerService</span></span>](./Update-AzureRmContainerService.md)


