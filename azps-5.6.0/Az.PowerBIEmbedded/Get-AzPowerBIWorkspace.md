---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PowerBIEmbedded.dll-Help.xml
Module Name: Az.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/powershell/module/az.powerbiembedded/get-azpowerbiworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Get-AzPowerBIWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Get-AzPowerBIWorkspace.md
ms.openlocfilehash: d9c93bc487817d99b217519453dea10543852a1b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101907577"
---
# <span data-ttu-id="c1a39-101">Get-AzPowerBIWorkspace</span><span class="sxs-lookup"><span data-stu-id="c1a39-101">Get-AzPowerBIWorkspace</span></span>

## <span data-ttu-id="c1a39-102">簡介</span><span class="sxs-lookup"><span data-stu-id="c1a39-102">SYNOPSIS</span></span>
<span data-ttu-id="c1a39-103">在 Power BI 工作區集合中獲取工作區。</span><span class="sxs-lookup"><span data-stu-id="c1a39-103">Gets the workspaces in a Power BI workspace collection.</span></span>

## <span data-ttu-id="c1a39-104">語法</span><span class="sxs-lookup"><span data-stu-id="c1a39-104">SYNTAX</span></span>

```
Get-AzPowerBIWorkspace [-ResourceGroupName] <String> [-WorkspaceCollectionName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c1a39-105">描述</span><span class="sxs-lookup"><span data-stu-id="c1a39-105">DESCRIPTION</span></span>
<span data-ttu-id="c1a39-106">**Get-AzPowerBIWorkspace** Cmdlet 會取得 Power BI 工作區集合中的工作區。</span><span class="sxs-lookup"><span data-stu-id="c1a39-106">The **Get-AzPowerBIWorkspace** cmdlet gets the workspaces in a Power BI workspace collection.</span></span>

## <span data-ttu-id="c1a39-107">例子</span><span class="sxs-lookup"><span data-stu-id="c1a39-107">EXAMPLES</span></span>

### <span data-ttu-id="c1a39-108">範例 1：取得工作區集合的工作區</span><span class="sxs-lookup"><span data-stu-id="c1a39-108">Example 1: Get workspaces of a workspace collection</span></span>
```
PS C:\>Get-AzPowerBIWorkspace -ResourceGroupName "ResourceGroup17" -WorkspaceCollectionName "WCN11"
```

<span data-ttu-id="c1a39-109">此命令會獲得屬於指定資源群組中名為 WCN11 之工作區集合的工作區。</span><span class="sxs-lookup"><span data-stu-id="c1a39-109">This command gets the workspaces that belong to the workspace collection named WCN11 in the specified resource group.</span></span>

## <span data-ttu-id="c1a39-110">參數</span><span class="sxs-lookup"><span data-stu-id="c1a39-110">PARAMETERS</span></span>

### <span data-ttu-id="c1a39-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1a39-111">-DefaultProfile</span></span>
<span data-ttu-id="c1a39-112">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="c1a39-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c1a39-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c1a39-113">-ResourceGroupName</span></span>
<span data-ttu-id="c1a39-114">指定工作區集合所屬的資源組名。</span><span class="sxs-lookup"><span data-stu-id="c1a39-114">Specifies the name of the resource group to which the workspace collection belongs.</span></span>

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

### <span data-ttu-id="c1a39-115">-WorkspaceCollectionName</span><span class="sxs-lookup"><span data-stu-id="c1a39-115">-WorkspaceCollectionName</span></span>
<span data-ttu-id="c1a39-116">指定此 Cmdlet 可獲取工作區的工作區集合名稱。</span><span class="sxs-lookup"><span data-stu-id="c1a39-116">Specifies the name of the workspace collection for which this cmdlet gets workspaces.</span></span>

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

### <span data-ttu-id="c1a39-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1a39-117">CommonParameters</span></span>
<span data-ttu-id="c1a39-118">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="c1a39-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1a39-119">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="c1a39-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1a39-120">輸入</span><span class="sxs-lookup"><span data-stu-id="c1a39-120">INPUTS</span></span>

### <span data-ttu-id="c1a39-121">System.String</span><span class="sxs-lookup"><span data-stu-id="c1a39-121">System.String</span></span>

## <span data-ttu-id="c1a39-122">輸出</span><span class="sxs-lookup"><span data-stu-id="c1a39-122">OUTPUTS</span></span>

### <span data-ttu-id="c1a39-123">Microsoft.Azure.Commands.management.PowerBIEmbedded.models.PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="c1a39-123">Microsoft.Azure.Commands.Management.PowerBIEmbedded.Models.PSWorkspace</span></span>

## <span data-ttu-id="c1a39-124">筆記</span><span class="sxs-lookup"><span data-stu-id="c1a39-124">NOTES</span></span>

## <span data-ttu-id="c1a39-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="c1a39-125">RELATED LINKS</span></span>

[<span data-ttu-id="c1a39-126">Get-AzPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="c1a39-126">Get-AzPowerBIWorkspaceCollection</span></span>](./Get-AzPowerBIWorkspaceCollection.md)


