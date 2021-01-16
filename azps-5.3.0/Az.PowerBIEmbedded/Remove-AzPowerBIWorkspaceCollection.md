---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PowerBIEmbedded.dll-Help.xml
Module Name: Az.PowerBIEmbedded
ms.assetid: 2D63CC6D-AB02-4299-A922-4057D6F595D7
online version: https://docs.microsoft.com/en-us/powershell/module/az.powerbiembedded/remove-azpowerbiworkspacecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Remove-AzPowerBIWorkspaceCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Remove-AzPowerBIWorkspaceCollection.md
ms.openlocfilehash: c8e6f54b5bd4deeb4ef24559298306880740c6d3
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98435677"
---
# <span data-ttu-id="ef0ee-101">Remove-AzPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="ef0ee-101">Remove-AzPowerBIWorkspaceCollection</span></span>

## <span data-ttu-id="ef0ee-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ef0ee-102">SYNOPSIS</span></span>
<span data-ttu-id="ef0ee-103">移除 Power BI 工作區集合。</span><span class="sxs-lookup"><span data-stu-id="ef0ee-103">Removes a Power BI workspace collection.</span></span>

## <span data-ttu-id="ef0ee-104">句法</span><span class="sxs-lookup"><span data-stu-id="ef0ee-104">SYNTAX</span></span>

```
Remove-AzPowerBIWorkspaceCollection [-ResourceGroupName] <String> [-WorkspaceCollectionName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ef0ee-105">說明</span><span class="sxs-lookup"><span data-stu-id="ef0ee-105">DESCRIPTION</span></span>
<span data-ttu-id="ef0ee-106">**AzPowerBIWorkspaceCollection** Cmdlet 會從您的 Azure 訂閱和資源群組中移除 Power BI 工作區集合。</span><span class="sxs-lookup"><span data-stu-id="ef0ee-106">The **Remove-AzPowerBIWorkspaceCollection** cmdlet removes a Power BI workspace collection from your Azure subscription and resource group.</span></span>

## <span data-ttu-id="ef0ee-107">示例</span><span class="sxs-lookup"><span data-stu-id="ef0ee-107">EXAMPLES</span></span>

### <span data-ttu-id="ef0ee-108">範例1：移除工作區集合</span><span class="sxs-lookup"><span data-stu-id="ef0ee-108">Example 1: Remove a workspace collection</span></span>
```
PS C:\>Remove-AzPowerBIWorkspaceCollection -ResourceGroupName "ResourceGroup17" -WorkspaceCollectionName "WCN11"
```

<span data-ttu-id="ef0ee-109">這個命令會從指定的資源群組中移除名為 WCN11 的工作區集合。</span><span class="sxs-lookup"><span data-stu-id="ef0ee-109">This command removes the workspace collection named WCN11 in the specified resource group.</span></span>

## <span data-ttu-id="ef0ee-110">參數</span><span class="sxs-lookup"><span data-stu-id="ef0ee-110">PARAMETERS</span></span>

### <span data-ttu-id="ef0ee-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef0ee-111">-DefaultProfile</span></span>
<span data-ttu-id="ef0ee-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="ef0ee-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ef0ee-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ef0ee-113">-ResourceGroupName</span></span>
<span data-ttu-id="ef0ee-114">指定此 Cmdlet 從中移除工作區集合之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="ef0ee-114">Specifies the name of the resource group from which this cmdlet removes a workspace collection.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ef0ee-115">-WorkspaceCollectionName</span><span class="sxs-lookup"><span data-stu-id="ef0ee-115">-WorkspaceCollectionName</span></span>
<span data-ttu-id="ef0ee-116">指定此 Cmdlet 移除的 Power BI workspace 集合的名稱。</span><span class="sxs-lookup"><span data-stu-id="ef0ee-116">Specifies the name of the Power BI workspace collection that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ef0ee-117">-確認</span><span class="sxs-lookup"><span data-stu-id="ef0ee-117">-Confirm</span></span>
<span data-ttu-id="ef0ee-118">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="ef0ee-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ef0ee-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ef0ee-119">-WhatIf</span></span>
<span data-ttu-id="ef0ee-120">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ef0ee-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ef0ee-121">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ef0ee-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ef0ee-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef0ee-122">CommonParameters</span></span>
<span data-ttu-id="ef0ee-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ef0ee-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef0ee-124">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="ef0ee-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef0ee-125">輸入</span><span class="sxs-lookup"><span data-stu-id="ef0ee-125">INPUTS</span></span>

### <span data-ttu-id="ef0ee-126">System.object</span><span class="sxs-lookup"><span data-stu-id="ef0ee-126">System.String</span></span>

## <span data-ttu-id="ef0ee-127">輸出</span><span class="sxs-lookup"><span data-stu-id="ef0ee-127">OUTPUTS</span></span>

### <span data-ttu-id="ef0ee-128">System.void</span><span class="sxs-lookup"><span data-stu-id="ef0ee-128">System.Void</span></span>

## <span data-ttu-id="ef0ee-129">筆記</span><span class="sxs-lookup"><span data-stu-id="ef0ee-129">NOTES</span></span>

## <span data-ttu-id="ef0ee-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="ef0ee-130">RELATED LINKS</span></span>

[<span data-ttu-id="ef0ee-131">AzPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="ef0ee-131">Get-AzPowerBIWorkspaceCollection</span></span>](./Get-AzPowerBIWorkspaceCollection.md)

[<span data-ttu-id="ef0ee-132">新-AzPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="ef0ee-132">New-AzPowerBIWorkspaceCollection</span></span>](./New-AzPowerBIWorkspaceCollection.md)


