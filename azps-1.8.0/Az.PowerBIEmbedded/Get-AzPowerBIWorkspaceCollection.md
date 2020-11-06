---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PowerBIEmbedded.dll-Help.xml
Module Name: Az.PowerBIEmbedded
ms.assetid: EEF32F48-00F6-4C57-B4F1-B58B566EAFEF
online version: https://docs.microsoft.com/en-us/powershell/module/az.powerbiembedded/get-azpowerbiworkspacecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Get-AzPowerBIWorkspaceCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Get-AzPowerBIWorkspaceCollection.md
ms.openlocfilehash: 19b1d1b0da719167d53739a8c92a97121656aa9a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93621258"
---
# <span data-ttu-id="87e3e-101">Get-AzPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="87e3e-101">Get-AzPowerBIWorkspaceCollection</span></span>

## <span data-ttu-id="87e3e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="87e3e-102">SYNOPSIS</span></span>
<span data-ttu-id="87e3e-103">取得 Power BI 工作區集合。</span><span class="sxs-lookup"><span data-stu-id="87e3e-103">Gets Power BI workspace collections.</span></span>

## <span data-ttu-id="87e3e-104">句法</span><span class="sxs-lookup"><span data-stu-id="87e3e-104">SYNTAX</span></span>

### <span data-ttu-id="87e3e-105">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="87e3e-105">ResourceGroupParameterSet</span></span>
```
Get-AzPowerBIWorkspaceCollection [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="87e3e-106">WorkspaceCollectionNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="87e3e-106">WorkspaceCollectionNameParameterSet</span></span>
```
Get-AzPowerBIWorkspaceCollection [-ResourceGroupName] <String> [-WorkspaceCollectionName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="87e3e-107">說明</span><span class="sxs-lookup"><span data-stu-id="87e3e-107">DESCRIPTION</span></span>
<span data-ttu-id="87e3e-108">**AzPowerBIWorkspaceCollection** Cmdlet 會在您的 Azure 訂閱和資源群組中取得 Power BI 工作區集合，或依集合名稱取得。</span><span class="sxs-lookup"><span data-stu-id="87e3e-108">The **Get-AzPowerBIWorkspaceCollection** cmdlet gets Power BI workspace collections in your Azure subscription and resource group, or by collection name.</span></span>

## <span data-ttu-id="87e3e-109">示例</span><span class="sxs-lookup"><span data-stu-id="87e3e-109">EXAMPLES</span></span>

### <span data-ttu-id="87e3e-110">範例1：取得資源群組中的所有工作區集合</span><span class="sxs-lookup"><span data-stu-id="87e3e-110">Example 1: Get all workspace collections in a resource group</span></span>
```
PS C:\>Get-AzPowerBIWorkspaceCollection -ResourceGroupName "ResourceGroup17"
```

<span data-ttu-id="87e3e-111">這個命令會取得屬於名為 ResourceGroup17 之資源群組的工作區集合。</span><span class="sxs-lookup"><span data-stu-id="87e3e-111">This command gets the workspace collections that belong to the resource group named ResourceGroup17.</span></span>

### <span data-ttu-id="87e3e-112">範例2：使用其名稱取得工作區集合</span><span class="sxs-lookup"><span data-stu-id="87e3e-112">Example 2: Get a workspace collection by using its name</span></span>
```
PS C:\>Get-AzPowerBIWorkspaceCollection -ResourceGroupName "ResourceGroup17" -WorkspaceCollectionName "WCN11"
```

<span data-ttu-id="87e3e-113">這個命令會在指定的資源群組中取得名為 WCN11 的工作區集合。</span><span class="sxs-lookup"><span data-stu-id="87e3e-113">This command gets the workspace collection named WCN11 in the specified resource group.</span></span>

## <span data-ttu-id="87e3e-114">參數</span><span class="sxs-lookup"><span data-stu-id="87e3e-114">PARAMETERS</span></span>

### <span data-ttu-id="87e3e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87e3e-115">-DefaultProfile</span></span>
<span data-ttu-id="87e3e-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="87e3e-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="87e3e-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="87e3e-117">-ResourceGroupName</span></span>
<span data-ttu-id="87e3e-118">指定此 Cmdlet 取得工作區集合之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="87e3e-118">Specifies the name of the resource group from which this cmdlet gets workspace collections.</span></span>

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

### <span data-ttu-id="87e3e-119">-WorkspaceCollectionName</span><span class="sxs-lookup"><span data-stu-id="87e3e-119">-WorkspaceCollectionName</span></span>
<span data-ttu-id="87e3e-120">指定此 Cmdlet 所取得的 Power BI workspace 集合的名稱。</span><span class="sxs-lookup"><span data-stu-id="87e3e-120">Specifies the name of the Power BI workspace collection that this cmdlet gets.</span></span>

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

### <span data-ttu-id="87e3e-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87e3e-121">CommonParameters</span></span>
<span data-ttu-id="87e3e-122">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="87e3e-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87e3e-123">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="87e3e-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87e3e-124">輸入</span><span class="sxs-lookup"><span data-stu-id="87e3e-124">INPUTS</span></span>

### <span data-ttu-id="87e3e-125">System.object</span><span class="sxs-lookup"><span data-stu-id="87e3e-125">System.String</span></span>

## <span data-ttu-id="87e3e-126">輸出</span><span class="sxs-lookup"><span data-stu-id="87e3e-126">OUTPUTS</span></span>

### <span data-ttu-id="87e3e-127">PSWorkspaceCollection （PowerBIEmbedded.）。</span><span class="sxs-lookup"><span data-stu-id="87e3e-127">Microsoft.Azure.Commands.Management.PowerBIEmbedded.Models.PSWorkspaceCollection</span></span>

## <span data-ttu-id="87e3e-128">筆記</span><span class="sxs-lookup"><span data-stu-id="87e3e-128">NOTES</span></span>

## <span data-ttu-id="87e3e-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="87e3e-129">RELATED LINKS</span></span>

[<span data-ttu-id="87e3e-130">新-AzPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="87e3e-130">New-AzPowerBIWorkspaceCollection</span></span>](./New-AzPowerBIWorkspaceCollection.md)

[<span data-ttu-id="87e3e-131">移除-AzPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="87e3e-131">Remove-AzPowerBIWorkspaceCollection</span></span>](./Remove-AzPowerBIWorkspaceCollection.md)


