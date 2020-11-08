---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PowerBIEmbedded.dll-Help.xml
Module Name: Az.PowerBIEmbedded
ms.assetid: 9F9E4273-6747-4963-AF1F-C0AEB46770A4
online version: https://docs.microsoft.com/en-us/powershell/module/az.powerbiembedded/new-azpowerbiworkspacecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/New-AzPowerBIWorkspaceCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/New-AzPowerBIWorkspaceCollection.md
ms.openlocfilehash: 557b1b7c5c2a91ec5e77729e70d2aa58f696d212
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93956566"
---
# <span data-ttu-id="3f54d-101">New-AzPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="3f54d-101">New-AzPowerBIWorkspaceCollection</span></span>

## <span data-ttu-id="3f54d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="3f54d-102">SYNOPSIS</span></span>
<span data-ttu-id="3f54d-103">建立 Power BI 工作區集合。</span><span class="sxs-lookup"><span data-stu-id="3f54d-103">Creates a Power BI workspace collection.</span></span>

## <span data-ttu-id="3f54d-104">句法</span><span class="sxs-lookup"><span data-stu-id="3f54d-104">SYNTAX</span></span>

```
New-AzPowerBIWorkspaceCollection [-ResourceGroupName] <String> [-WorkspaceCollectionName] <String>
 [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3f54d-105">說明</span><span class="sxs-lookup"><span data-stu-id="3f54d-105">DESCRIPTION</span></span>
<span data-ttu-id="3f54d-106">**新的-AzPowerBIWorkspaceCollection** Cmdlet 會在指定的資源群組和位置中為您的 Azure 訂閱建立 Power BI 工作區集合。</span><span class="sxs-lookup"><span data-stu-id="3f54d-106">The **New-AzPowerBIWorkspaceCollection** cmdlet creates a Power BI workspace collection for your Azure subscription in the specified resource group and location.</span></span>

## <span data-ttu-id="3f54d-107">示例</span><span class="sxs-lookup"><span data-stu-id="3f54d-107">EXAMPLES</span></span>

### <span data-ttu-id="3f54d-108">範例1：建立工作區集合</span><span class="sxs-lookup"><span data-stu-id="3f54d-108">Example 1: Create a workspace collection</span></span>
```
PS C:\>New-AzPowerBIWorkspaceCollection -ResourceGroupName "ResourceGroup17" -WorkspaceCollectionName "WCN11" -Location "Japan West"
```

<span data-ttu-id="3f54d-109">這個命令會在指定的資源群組的指定位置中，建立名為 WCN11 的工作區集合。</span><span class="sxs-lookup"><span data-stu-id="3f54d-109">This command creates a workspace collection named WCN11 in the specified resource group in the specified location.</span></span>

## <span data-ttu-id="3f54d-110">參數</span><span class="sxs-lookup"><span data-stu-id="3f54d-110">PARAMETERS</span></span>

### <span data-ttu-id="3f54d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f54d-111">-DefaultProfile</span></span>
<span data-ttu-id="3f54d-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="3f54d-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3f54d-113">-位置</span><span class="sxs-lookup"><span data-stu-id="3f54d-113">-Location</span></span>
<span data-ttu-id="3f54d-114">指定此 Cmdlet 建立工作區集合的 Azure 位置。</span><span class="sxs-lookup"><span data-stu-id="3f54d-114">Specifies the Azure location in which this cmdlet creates a workspace collection.</span></span>

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

### <span data-ttu-id="3f54d-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3f54d-115">-ResourceGroupName</span></span>
<span data-ttu-id="3f54d-116">指定此 Cmdlet 建立工作區集合之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="3f54d-116">Specifies the name of the resource group in which this cmdlet creates a workspace collection.</span></span>

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

### <span data-ttu-id="3f54d-117">-WorkspaceCollectionName</span><span class="sxs-lookup"><span data-stu-id="3f54d-117">-WorkspaceCollectionName</span></span>
<span data-ttu-id="3f54d-118">指定 Power BI 工作區集合的名稱。</span><span class="sxs-lookup"><span data-stu-id="3f54d-118">Specifies a name for the Power BI workspace collection.</span></span>

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

### <span data-ttu-id="3f54d-119">-確認</span><span class="sxs-lookup"><span data-stu-id="3f54d-119">-Confirm</span></span>
<span data-ttu-id="3f54d-120">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="3f54d-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3f54d-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3f54d-121">-WhatIf</span></span>
<span data-ttu-id="3f54d-122">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="3f54d-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3f54d-123">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="3f54d-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3f54d-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f54d-124">CommonParameters</span></span>
<span data-ttu-id="3f54d-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="3f54d-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f54d-126">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="3f54d-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f54d-127">輸入</span><span class="sxs-lookup"><span data-stu-id="3f54d-127">INPUTS</span></span>

### <span data-ttu-id="3f54d-128">System.object</span><span class="sxs-lookup"><span data-stu-id="3f54d-128">System.String</span></span>

## <span data-ttu-id="3f54d-129">輸出</span><span class="sxs-lookup"><span data-stu-id="3f54d-129">OUTPUTS</span></span>

### <span data-ttu-id="3f54d-130">PSWorkspaceCollection （PowerBIEmbedded.）。</span><span class="sxs-lookup"><span data-stu-id="3f54d-130">Microsoft.Azure.Commands.Management.PowerBIEmbedded.Models.PSWorkspaceCollection</span></span>

## <span data-ttu-id="3f54d-131">筆記</span><span class="sxs-lookup"><span data-stu-id="3f54d-131">NOTES</span></span>

## <span data-ttu-id="3f54d-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="3f54d-132">RELATED LINKS</span></span>

[<span data-ttu-id="3f54d-133">AzPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="3f54d-133">Get-AzPowerBIWorkspaceCollection</span></span>](./Get-AzPowerBIWorkspaceCollection.md)

[<span data-ttu-id="3f54d-134">移除-AzPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="3f54d-134">Remove-AzPowerBIWorkspaceCollection</span></span>](./Remove-AzPowerBIWorkspaceCollection.md)

