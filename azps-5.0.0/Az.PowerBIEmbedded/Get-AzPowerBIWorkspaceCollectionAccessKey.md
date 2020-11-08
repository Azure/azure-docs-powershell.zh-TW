---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PowerBIEmbedded.dll-Help.xml
Module Name: Az.PowerBIEmbedded
ms.assetid: 3FED0088-47DA-4565-B9F0-DACF9B2DC0C7
online version: https://docs.microsoft.com/en-us/powershell/module/az.powerbiembedded/get-azpowerbiworkspacecollectionaccesskey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Get-AzPowerBIWorkspaceCollectionAccessKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Get-AzPowerBIWorkspaceCollectionAccessKey.md
ms.openlocfilehash: 9108f224297b23fd391e1a4c3afac4b826aa3dbf
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94137367"
---
# <span data-ttu-id="b52da-101">Get-AzPowerBIWorkspaceCollectionAccessKey</span><span class="sxs-lookup"><span data-stu-id="b52da-101">Get-AzPowerBIWorkspaceCollectionAccessKey</span></span>

## <span data-ttu-id="b52da-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b52da-102">SYNOPSIS</span></span>
<span data-ttu-id="b52da-103">取得與 Power BI 工作區集合相關聯的目前便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="b52da-103">Gets the current access keys associated with a Power BI workspace collection.</span></span>

## <span data-ttu-id="b52da-104">句法</span><span class="sxs-lookup"><span data-stu-id="b52da-104">SYNTAX</span></span>

```
Get-AzPowerBIWorkspaceCollectionAccessKey [-ResourceGroupName] <String> [-WorkspaceCollectionName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b52da-105">說明</span><span class="sxs-lookup"><span data-stu-id="b52da-105">DESCRIPTION</span></span>
<span data-ttu-id="b52da-106">**AzPowerBIWorkspaceCollectionAccessKey** Cmdlet 會取得與 Power BI 工作區集合相關聯的目前便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="b52da-106">The **Get-AzPowerBIWorkspaceCollectionAccessKey** cmdlet gets the current access keys associated with a Power BI workspace collection.</span></span>

## <span data-ttu-id="b52da-107">示例</span><span class="sxs-lookup"><span data-stu-id="b52da-107">EXAMPLES</span></span>

### <span data-ttu-id="b52da-108">範例1：取得便捷鍵</span><span class="sxs-lookup"><span data-stu-id="b52da-108">Example 1: Get access keys</span></span>
```
PS C:\>Get-AzPowerBIWorkspaceCollectionAccessKey -ResourceGroupName "ResourceGroup17" -WorkspaceCollectionName "WCN11"
```

<span data-ttu-id="b52da-109">這個命令會取得指定資源群組中名為 WCN11 的工作區集合的便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="b52da-109">This command gets access keys for the workspace collection named WCN11 in the specified resource group.</span></span>

## <span data-ttu-id="b52da-110">參數</span><span class="sxs-lookup"><span data-stu-id="b52da-110">PARAMETERS</span></span>

### <span data-ttu-id="b52da-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b52da-111">-DefaultProfile</span></span>
<span data-ttu-id="b52da-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="b52da-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b52da-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b52da-113">-ResourceGroupName</span></span>
<span data-ttu-id="b52da-114">指定集合之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="b52da-114">Specifies the name of the resource group of the collection.</span></span>

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

### <span data-ttu-id="b52da-115">-WorkspaceCollectionName</span><span class="sxs-lookup"><span data-stu-id="b52da-115">-WorkspaceCollectionName</span></span>
<span data-ttu-id="b52da-116">指定此 Cmdlet 在其上執行的 Power BI 工作區集合的名稱。</span><span class="sxs-lookup"><span data-stu-id="b52da-116">Specifies the name of the Power BI workspace collection on which this cmdlet operates.</span></span>

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

### <span data-ttu-id="b52da-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b52da-117">CommonParameters</span></span>
<span data-ttu-id="b52da-118">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b52da-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b52da-119">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="b52da-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b52da-120">輸入</span><span class="sxs-lookup"><span data-stu-id="b52da-120">INPUTS</span></span>

### <span data-ttu-id="b52da-121">System.object</span><span class="sxs-lookup"><span data-stu-id="b52da-121">System.String</span></span>

## <span data-ttu-id="b52da-122">輸出</span><span class="sxs-lookup"><span data-stu-id="b52da-122">OUTPUTS</span></span>

### <span data-ttu-id="b52da-123">PSWorkspaceCollectionAccessKey （PowerBIEmbedded.）。</span><span class="sxs-lookup"><span data-stu-id="b52da-123">Microsoft.Azure.Commands.Management.PowerBIEmbedded.Models.PSWorkspaceCollectionAccessKey</span></span>

## <span data-ttu-id="b52da-124">筆記</span><span class="sxs-lookup"><span data-stu-id="b52da-124">NOTES</span></span>

## <span data-ttu-id="b52da-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="b52da-125">RELATED LINKS</span></span>

[<span data-ttu-id="b52da-126">Reset-AzPowerBIWorkspaceCollectionAccessKey</span><span class="sxs-lookup"><span data-stu-id="b52da-126">Reset-AzPowerBIWorkspaceCollectionAccessKey</span></span>](./Reset-AzPowerBIWorkspaceCollectionAccessKey.md)


