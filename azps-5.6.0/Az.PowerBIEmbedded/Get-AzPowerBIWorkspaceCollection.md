---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PowerBIEmbedded.dll-Help.xml
Module Name: Az.PowerBIEmbedded
ms.assetid: EEF32F48-00F6-4C57-B4F1-B58B566EAFEF
online version: https://docs.microsoft.com/powershell/module/az.powerbiembedded/get-azpowerbiworkspacecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Get-AzPowerBIWorkspaceCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Get-AzPowerBIWorkspaceCollection.md
ms.openlocfilehash: 99a9d8e4dcf10eaae67516e871c90d78021e6218
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101902289"
---
# <span data-ttu-id="92742-101">Get-AzPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="92742-101">Get-AzPowerBIWorkspaceCollection</span></span>

## <span data-ttu-id="92742-102">簡介</span><span class="sxs-lookup"><span data-stu-id="92742-102">SYNOPSIS</span></span>
<span data-ttu-id="92742-103">獲得 Power BI 工作區集合。</span><span class="sxs-lookup"><span data-stu-id="92742-103">Gets Power BI workspace collections.</span></span>

## <span data-ttu-id="92742-104">語法</span><span class="sxs-lookup"><span data-stu-id="92742-104">SYNTAX</span></span>

### <span data-ttu-id="92742-105">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="92742-105">ResourceGroupParameterSet</span></span>
```
Get-AzPowerBIWorkspaceCollection [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="92742-106">WorkspaceCollectionNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="92742-106">WorkspaceCollectionNameParameterSet</span></span>
```
Get-AzPowerBIWorkspaceCollection [-ResourceGroupName] <String> [-WorkspaceCollectionName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="92742-107">描述</span><span class="sxs-lookup"><span data-stu-id="92742-107">DESCRIPTION</span></span>
<span data-ttu-id="92742-108">**Get-AzPowerBIWorkspaceCollection** Cmdlet 會取得 Azure 訂閱和資源群組中的 Power BI 工作區集合，或按集合名稱。</span><span class="sxs-lookup"><span data-stu-id="92742-108">The **Get-AzPowerBIWorkspaceCollection** cmdlet gets Power BI workspace collections in your Azure subscription and resource group, or by collection name.</span></span>

## <span data-ttu-id="92742-109">例子</span><span class="sxs-lookup"><span data-stu-id="92742-109">EXAMPLES</span></span>

### <span data-ttu-id="92742-110">範例 1：在資源群組中取得所有工作區集合</span><span class="sxs-lookup"><span data-stu-id="92742-110">Example 1: Get all workspace collections in a resource group</span></span>
```
PS C:\>Get-AzPowerBIWorkspaceCollection -ResourceGroupName "ResourceGroup17"
```

<span data-ttu-id="92742-111">此命令會獲得屬於 ResourceGroup17 資源群組的工作區集合。</span><span class="sxs-lookup"><span data-stu-id="92742-111">This command gets the workspace collections that belong to the resource group named ResourceGroup17.</span></span>

### <span data-ttu-id="92742-112">範例 2：使用工作區集合的名稱取得</span><span class="sxs-lookup"><span data-stu-id="92742-112">Example 2: Get a workspace collection by using its name</span></span>
```
PS C:\>Get-AzPowerBIWorkspaceCollection -ResourceGroupName "ResourceGroup17" -WorkspaceCollectionName "WCN11"
```

<span data-ttu-id="92742-113">此命令會獲得指定資源群組中名為 WCN11 的工作區集合。</span><span class="sxs-lookup"><span data-stu-id="92742-113">This command gets the workspace collection named WCN11 in the specified resource group.</span></span>

## <span data-ttu-id="92742-114">參數</span><span class="sxs-lookup"><span data-stu-id="92742-114">PARAMETERS</span></span>

### <span data-ttu-id="92742-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92742-115">-DefaultProfile</span></span>
<span data-ttu-id="92742-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="92742-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="92742-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="92742-117">-ResourceGroupName</span></span>
<span data-ttu-id="92742-118">指定此 Cmdlet 從其中獲得工作區集合的資源組名。</span><span class="sxs-lookup"><span data-stu-id="92742-118">Specifies the name of the resource group from which this cmdlet gets workspace collections.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: WorkspaceCollectionNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="92742-119">-WorkspaceCollectionName</span><span class="sxs-lookup"><span data-stu-id="92742-119">-WorkspaceCollectionName</span></span>
<span data-ttu-id="92742-120">指定此 Cmdlet 所獲得之 Power BI 工作區集合的名稱。</span><span class="sxs-lookup"><span data-stu-id="92742-120">Specifies the name of the Power BI workspace collection that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: WorkspaceCollectionNameParameterSet
Aliases: Name, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="92742-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92742-121">CommonParameters</span></span>
<span data-ttu-id="92742-122">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="92742-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92742-123">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="92742-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92742-124">輸入</span><span class="sxs-lookup"><span data-stu-id="92742-124">INPUTS</span></span>

### <span data-ttu-id="92742-125">System.String</span><span class="sxs-lookup"><span data-stu-id="92742-125">System.String</span></span>

## <span data-ttu-id="92742-126">輸出</span><span class="sxs-lookup"><span data-stu-id="92742-126">OUTPUTS</span></span>

### <span data-ttu-id="92742-127">Microsoft.Azure.Commands.management.PowerBIEmbedded.models.PSWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="92742-127">Microsoft.Azure.Commands.Management.PowerBIEmbedded.Models.PSWorkspaceCollection</span></span>

## <span data-ttu-id="92742-128">筆記</span><span class="sxs-lookup"><span data-stu-id="92742-128">NOTES</span></span>

## <span data-ttu-id="92742-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="92742-129">RELATED LINKS</span></span>

[<span data-ttu-id="92742-130">New-AzPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="92742-130">New-AzPowerBIWorkspaceCollection</span></span>](./New-AzPowerBIWorkspaceCollection.md)

[<span data-ttu-id="92742-131">Remove-AzPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="92742-131">Remove-AzPowerBIWorkspaceCollection</span></span>](./Remove-AzPowerBIWorkspaceCollection.md)


