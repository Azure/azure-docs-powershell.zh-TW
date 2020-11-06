---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PowerBIEmbedded.dll-Help.xml
Module Name: Az.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/en-us/powershell/module/az.powerbiembedded/get-azpowerbiworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Get-AzPowerBIWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Get-AzPowerBIWorkspace.md
ms.openlocfilehash: 0bba0651d8b1125673b97aea625a11e598db6c85
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93621264"
---
# <span data-ttu-id="95f32-101">Get-AzPowerBIWorkspace</span><span class="sxs-lookup"><span data-stu-id="95f32-101">Get-AzPowerBIWorkspace</span></span>

## <span data-ttu-id="95f32-102">摘要</span><span class="sxs-lookup"><span data-stu-id="95f32-102">SYNOPSIS</span></span>
<span data-ttu-id="95f32-103">在 Power BI 工作區集合中取得工作區。</span><span class="sxs-lookup"><span data-stu-id="95f32-103">Gets the workspaces in a Power BI workspace collection.</span></span>

## <span data-ttu-id="95f32-104">句法</span><span class="sxs-lookup"><span data-stu-id="95f32-104">SYNTAX</span></span>

```
Get-AzPowerBIWorkspace [-ResourceGroupName] <String> [-WorkspaceCollectionName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="95f32-105">說明</span><span class="sxs-lookup"><span data-stu-id="95f32-105">DESCRIPTION</span></span>
<span data-ttu-id="95f32-106">**AzPowerBIWorkspace** Cmdlet 會取得 Power BI 工作區集合中的工作區。</span><span class="sxs-lookup"><span data-stu-id="95f32-106">The **Get-AzPowerBIWorkspace** cmdlet gets the workspaces in a Power BI workspace collection.</span></span>

## <span data-ttu-id="95f32-107">示例</span><span class="sxs-lookup"><span data-stu-id="95f32-107">EXAMPLES</span></span>

### <span data-ttu-id="95f32-108">範例1：取得工作區集合的工作區</span><span class="sxs-lookup"><span data-stu-id="95f32-108">Example 1: Get workspaces of a workspace collection</span></span>
```
PS C:\>Get-AzPowerBIWorkspace -ResourceGroupName "ResourceGroup17" -WorkspaceCollectionName "WCN11"
```

<span data-ttu-id="95f32-109">這個命令會在指定的資源群組中，取得屬於名為 WCN11 之工作區集合的工作區。</span><span class="sxs-lookup"><span data-stu-id="95f32-109">This command gets the workspaces that belong to the workspace collection named WCN11 in the specified resource group.</span></span>

## <span data-ttu-id="95f32-110">參數</span><span class="sxs-lookup"><span data-stu-id="95f32-110">PARAMETERS</span></span>

### <span data-ttu-id="95f32-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95f32-111">-DefaultProfile</span></span>
<span data-ttu-id="95f32-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="95f32-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="95f32-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="95f32-113">-ResourceGroupName</span></span>
<span data-ttu-id="95f32-114">指定工作區集合所屬之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="95f32-114">Specifies the name of the resource group to which the workspace collection belongs.</span></span>

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

### <span data-ttu-id="95f32-115">-WorkspaceCollectionName</span><span class="sxs-lookup"><span data-stu-id="95f32-115">-WorkspaceCollectionName</span></span>
<span data-ttu-id="95f32-116">指定此 Cmdlet 取得工作區之工作區集合的名稱。</span><span class="sxs-lookup"><span data-stu-id="95f32-116">Specifies the name of the workspace collection for which this cmdlet gets workspaces.</span></span>

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

### <span data-ttu-id="95f32-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95f32-117">CommonParameters</span></span>
<span data-ttu-id="95f32-118">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="95f32-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95f32-119">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="95f32-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95f32-120">輸入</span><span class="sxs-lookup"><span data-stu-id="95f32-120">INPUTS</span></span>

### <span data-ttu-id="95f32-121">System.object</span><span class="sxs-lookup"><span data-stu-id="95f32-121">System.String</span></span>

## <span data-ttu-id="95f32-122">輸出</span><span class="sxs-lookup"><span data-stu-id="95f32-122">OUTPUTS</span></span>

### <span data-ttu-id="95f32-123">PSWorkspace （PowerBIEmbedded.）。</span><span class="sxs-lookup"><span data-stu-id="95f32-123">Microsoft.Azure.Commands.Management.PowerBIEmbedded.Models.PSWorkspace</span></span>

## <span data-ttu-id="95f32-124">筆記</span><span class="sxs-lookup"><span data-stu-id="95f32-124">NOTES</span></span>

## <span data-ttu-id="95f32-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="95f32-125">RELATED LINKS</span></span>

[<span data-ttu-id="95f32-126">AzPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="95f32-126">Get-AzPowerBIWorkspaceCollection</span></span>](./Get-AzPowerBIWorkspaceCollection.md)


