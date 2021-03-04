---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PowerBIEmbedded.dll-Help.xml
Module Name: Az.PowerBIEmbedded
ms.assetid: 2D63CC6D-AB02-4299-A922-4057D6F595D7
online version: https://docs.microsoft.com/powershell/module/az.powerbiembedded/remove-azpowerbiworkspacecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Remove-AzPowerBIWorkspaceCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Remove-AzPowerBIWorkspaceCollection.md
ms.openlocfilehash: 1623b706a3878b517680782462e07ebacce2daf9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101902282"
---
# <span data-ttu-id="7cd67-101">Remove-AzPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="7cd67-101">Remove-AzPowerBIWorkspaceCollection</span></span>

## <span data-ttu-id="7cd67-102">簡介</span><span class="sxs-lookup"><span data-stu-id="7cd67-102">SYNOPSIS</span></span>
<span data-ttu-id="7cd67-103">移除 Power BI 工作區集合。</span><span class="sxs-lookup"><span data-stu-id="7cd67-103">Removes a Power BI workspace collection.</span></span>

## <span data-ttu-id="7cd67-104">語法</span><span class="sxs-lookup"><span data-stu-id="7cd67-104">SYNTAX</span></span>

```
Remove-AzPowerBIWorkspaceCollection [-ResourceGroupName] <String> [-WorkspaceCollectionName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7cd67-105">描述</span><span class="sxs-lookup"><span data-stu-id="7cd67-105">DESCRIPTION</span></span>
<span data-ttu-id="7cd67-106">**Remove-AzPowerBIWorkspaceCollection** Cmdlet 會從您的 Azure 訂閱和資源群組移除 Power BI 工作區集合。</span><span class="sxs-lookup"><span data-stu-id="7cd67-106">The **Remove-AzPowerBIWorkspaceCollection** cmdlet removes a Power BI workspace collection from your Azure subscription and resource group.</span></span>

## <span data-ttu-id="7cd67-107">例子</span><span class="sxs-lookup"><span data-stu-id="7cd67-107">EXAMPLES</span></span>

### <span data-ttu-id="7cd67-108">範例 1：移除工作區集合</span><span class="sxs-lookup"><span data-stu-id="7cd67-108">Example 1: Remove a workspace collection</span></span>
```
PS C:\>Remove-AzPowerBIWorkspaceCollection -ResourceGroupName "ResourceGroup17" -WorkspaceCollectionName "WCN11"
```

<span data-ttu-id="7cd67-109">此命令會移除指定資源群組中名為 WCN11 的工作區集合。</span><span class="sxs-lookup"><span data-stu-id="7cd67-109">This command removes the workspace collection named WCN11 in the specified resource group.</span></span>

## <span data-ttu-id="7cd67-110">參數</span><span class="sxs-lookup"><span data-stu-id="7cd67-110">PARAMETERS</span></span>

### <span data-ttu-id="7cd67-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7cd67-111">-DefaultProfile</span></span>
<span data-ttu-id="7cd67-112">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="7cd67-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7cd67-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7cd67-113">-ResourceGroupName</span></span>
<span data-ttu-id="7cd67-114">指定此 Cmdlet 移除工作區集合的資源組名。</span><span class="sxs-lookup"><span data-stu-id="7cd67-114">Specifies the name of the resource group from which this cmdlet removes a workspace collection.</span></span>

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

### <span data-ttu-id="7cd67-115">-WorkspaceCollectionName</span><span class="sxs-lookup"><span data-stu-id="7cd67-115">-WorkspaceCollectionName</span></span>
<span data-ttu-id="7cd67-116">指定此 Cmdlet 移除的 Power BI 工作區集合名稱。</span><span class="sxs-lookup"><span data-stu-id="7cd67-116">Specifies the name of the Power BI workspace collection that this cmdlet removes.</span></span>

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

### <span data-ttu-id="7cd67-117">-確認</span><span class="sxs-lookup"><span data-stu-id="7cd67-117">-Confirm</span></span>
<span data-ttu-id="7cd67-118">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="7cd67-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7cd67-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7cd67-119">-WhatIf</span></span>
<span data-ttu-id="7cd67-120">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="7cd67-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7cd67-121">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="7cd67-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7cd67-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7cd67-122">CommonParameters</span></span>
<span data-ttu-id="7cd67-123">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="7cd67-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7cd67-124">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="7cd67-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7cd67-125">輸入</span><span class="sxs-lookup"><span data-stu-id="7cd67-125">INPUTS</span></span>

### <span data-ttu-id="7cd67-126">System.String</span><span class="sxs-lookup"><span data-stu-id="7cd67-126">System.String</span></span>

## <span data-ttu-id="7cd67-127">輸出</span><span class="sxs-lookup"><span data-stu-id="7cd67-127">OUTPUTS</span></span>

### <span data-ttu-id="7cd67-128">System.Void</span><span class="sxs-lookup"><span data-stu-id="7cd67-128">System.Void</span></span>

## <span data-ttu-id="7cd67-129">筆記</span><span class="sxs-lookup"><span data-stu-id="7cd67-129">NOTES</span></span>

## <span data-ttu-id="7cd67-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="7cd67-130">RELATED LINKS</span></span>

[<span data-ttu-id="7cd67-131">Get-AzPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="7cd67-131">Get-AzPowerBIWorkspaceCollection</span></span>](./Get-AzPowerBIWorkspaceCollection.md)

[<span data-ttu-id="7cd67-132">New-AzPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="7cd67-132">New-AzPowerBIWorkspaceCollection</span></span>](./New-AzPowerBIWorkspaceCollection.md)


