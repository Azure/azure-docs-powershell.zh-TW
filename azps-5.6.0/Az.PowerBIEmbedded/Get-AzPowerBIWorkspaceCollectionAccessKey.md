---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PowerBIEmbedded.dll-Help.xml
Module Name: Az.PowerBIEmbedded
ms.assetid: 3FED0088-47DA-4565-B9F0-DACF9B2DC0C7
online version: https://docs.microsoft.com/powershell/module/az.powerbiembedded/get-azpowerbiworkspacecollectionaccesskey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Get-AzPowerBIWorkspaceCollectionAccessKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Get-AzPowerBIWorkspaceCollectionAccessKey.md
ms.openlocfilehash: 06e17c012f52883d5e160698bb6f858f4644af6a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101907574"
---
# <span data-ttu-id="dccbd-101">Get-AzPowerBIWorkspaceCollectionAccessKey</span><span class="sxs-lookup"><span data-stu-id="dccbd-101">Get-AzPowerBIWorkspaceCollectionAccessKey</span></span>

## <span data-ttu-id="dccbd-102">簡介</span><span class="sxs-lookup"><span data-stu-id="dccbd-102">SYNOPSIS</span></span>
<span data-ttu-id="dccbd-103">取得與 Power BI 工作區集合相關聯的目前便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="dccbd-103">Gets the current access keys associated with a Power BI workspace collection.</span></span>

## <span data-ttu-id="dccbd-104">語法</span><span class="sxs-lookup"><span data-stu-id="dccbd-104">SYNTAX</span></span>

```
Get-AzPowerBIWorkspaceCollectionAccessKey [-ResourceGroupName] <String> [-WorkspaceCollectionName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dccbd-105">描述</span><span class="sxs-lookup"><span data-stu-id="dccbd-105">DESCRIPTION</span></span>
<span data-ttu-id="dccbd-106">**Get-AzPowerBIWorkspaceCollectionAccessKey** Cmdlet 會取得與 Power BI 工作區集合相關聯的目前便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="dccbd-106">The **Get-AzPowerBIWorkspaceCollectionAccessKey** cmdlet gets the current access keys associated with a Power BI workspace collection.</span></span>

## <span data-ttu-id="dccbd-107">例子</span><span class="sxs-lookup"><span data-stu-id="dccbd-107">EXAMPLES</span></span>

### <span data-ttu-id="dccbd-108">範例 1：取得便捷鍵</span><span class="sxs-lookup"><span data-stu-id="dccbd-108">Example 1: Get access keys</span></span>
```
PS C:\>Get-AzPowerBIWorkspaceCollectionAccessKey -ResourceGroupName "ResourceGroup17" -WorkspaceCollectionName "WCN11"
```

<span data-ttu-id="dccbd-109">此命令會取得指定資源群組中名為 WCN11 的工作區集合便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="dccbd-109">This command gets access keys for the workspace collection named WCN11 in the specified resource group.</span></span>

## <span data-ttu-id="dccbd-110">參數</span><span class="sxs-lookup"><span data-stu-id="dccbd-110">PARAMETERS</span></span>

### <span data-ttu-id="dccbd-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dccbd-111">-DefaultProfile</span></span>
<span data-ttu-id="dccbd-112">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="dccbd-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="dccbd-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dccbd-113">-ResourceGroupName</span></span>
<span data-ttu-id="dccbd-114">指定集合的資源組名。</span><span class="sxs-lookup"><span data-stu-id="dccbd-114">Specifies the name of the resource group of the collection.</span></span>

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

### <span data-ttu-id="dccbd-115">-WorkspaceCollectionName</span><span class="sxs-lookup"><span data-stu-id="dccbd-115">-WorkspaceCollectionName</span></span>
<span data-ttu-id="dccbd-116">指定此 Cmdlet 操作之 Power BI 工作區集合的名稱。</span><span class="sxs-lookup"><span data-stu-id="dccbd-116">Specifies the name of the Power BI workspace collection on which this cmdlet operates.</span></span>

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

### <span data-ttu-id="dccbd-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dccbd-117">CommonParameters</span></span>
<span data-ttu-id="dccbd-118">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="dccbd-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dccbd-119">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="dccbd-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dccbd-120">輸入</span><span class="sxs-lookup"><span data-stu-id="dccbd-120">INPUTS</span></span>

### <span data-ttu-id="dccbd-121">System.String</span><span class="sxs-lookup"><span data-stu-id="dccbd-121">System.String</span></span>

## <span data-ttu-id="dccbd-122">輸出</span><span class="sxs-lookup"><span data-stu-id="dccbd-122">OUTPUTS</span></span>

### <span data-ttu-id="dccbd-123">Microsoft.Azure.Commands.management.PowerBIEmbedded.models.PSWorkspaceCollectionAccessKey</span><span class="sxs-lookup"><span data-stu-id="dccbd-123">Microsoft.Azure.Commands.Management.PowerBIEmbedded.Models.PSWorkspaceCollectionAccessKey</span></span>

## <span data-ttu-id="dccbd-124">筆記</span><span class="sxs-lookup"><span data-stu-id="dccbd-124">NOTES</span></span>

## <span data-ttu-id="dccbd-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="dccbd-125">RELATED LINKS</span></span>

[<span data-ttu-id="dccbd-126">Reset-AzPowerBIWorkspaceCollectionAccessKey</span><span class="sxs-lookup"><span data-stu-id="dccbd-126">Reset-AzPowerBIWorkspaceCollectionAccessKey</span></span>](./Reset-AzPowerBIWorkspaceCollectionAccessKey.md)


