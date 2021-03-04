---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PowerBIEmbedded.dll-Help.xml
Module Name: Az.PowerBIEmbedded
ms.assetid: 9F9E4273-6747-4963-AF1F-C0AEB46770A4
online version: https://docs.microsoft.com/powershell/module/az.powerbiembedded/new-azpowerbiworkspacecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/New-AzPowerBIWorkspaceCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/New-AzPowerBIWorkspaceCollection.md
ms.openlocfilehash: 69f90f84d7e142ea3471c7e6871baac145f1b9c0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101907554"
---
# <span data-ttu-id="f5ef1-101">New-AzPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="f5ef1-101">New-AzPowerBIWorkspaceCollection</span></span>

## <span data-ttu-id="f5ef1-102">簡介</span><span class="sxs-lookup"><span data-stu-id="f5ef1-102">SYNOPSIS</span></span>
<span data-ttu-id="f5ef1-103">建立 Power BI 工作區集合。</span><span class="sxs-lookup"><span data-stu-id="f5ef1-103">Creates a Power BI workspace collection.</span></span>

## <span data-ttu-id="f5ef1-104">語法</span><span class="sxs-lookup"><span data-stu-id="f5ef1-104">SYNTAX</span></span>

```
New-AzPowerBIWorkspaceCollection [-ResourceGroupName] <String> [-WorkspaceCollectionName] <String>
 [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f5ef1-105">描述</span><span class="sxs-lookup"><span data-stu-id="f5ef1-105">DESCRIPTION</span></span>
<span data-ttu-id="f5ef1-106">**New-AzPowerBIWorkspaceCollection** Cmdlet 會為指定的資源群組和位置中的 Azure 訂閱建立 Power BI 工作區集合。</span><span class="sxs-lookup"><span data-stu-id="f5ef1-106">The **New-AzPowerBIWorkspaceCollection** cmdlet creates a Power BI workspace collection for your Azure subscription in the specified resource group and location.</span></span>

## <span data-ttu-id="f5ef1-107">例子</span><span class="sxs-lookup"><span data-stu-id="f5ef1-107">EXAMPLES</span></span>

### <span data-ttu-id="f5ef1-108">範例 1：建立工作區集合</span><span class="sxs-lookup"><span data-stu-id="f5ef1-108">Example 1: Create a workspace collection</span></span>
```
PS C:\>New-AzPowerBIWorkspaceCollection -ResourceGroupName "ResourceGroup17" -WorkspaceCollectionName "WCN11" -Location "Japan West"
```

<span data-ttu-id="f5ef1-109">此命令會于指定位置的指定資源群組中建立名為 WCN11 的工作區集合。</span><span class="sxs-lookup"><span data-stu-id="f5ef1-109">This command creates a workspace collection named WCN11 in the specified resource group in the specified location.</span></span>

## <span data-ttu-id="f5ef1-110">參數</span><span class="sxs-lookup"><span data-stu-id="f5ef1-110">PARAMETERS</span></span>

### <span data-ttu-id="f5ef1-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5ef1-111">-DefaultProfile</span></span>
<span data-ttu-id="f5ef1-112">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="f5ef1-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f5ef1-113">-位置</span><span class="sxs-lookup"><span data-stu-id="f5ef1-113">-Location</span></span>
<span data-ttu-id="f5ef1-114">指定此 Cmdlet 建立工作區集合的 Azure 位置。</span><span class="sxs-lookup"><span data-stu-id="f5ef1-114">Specifies the Azure location in which this cmdlet creates a workspace collection.</span></span>

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

### <span data-ttu-id="f5ef1-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f5ef1-115">-ResourceGroupName</span></span>
<span data-ttu-id="f5ef1-116">指定此 Cmdlet 建立工作區集合的資源組名。</span><span class="sxs-lookup"><span data-stu-id="f5ef1-116">Specifies the name of the resource group in which this cmdlet creates a workspace collection.</span></span>

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

### <span data-ttu-id="f5ef1-117">-WorkspaceCollectionName</span><span class="sxs-lookup"><span data-stu-id="f5ef1-117">-WorkspaceCollectionName</span></span>
<span data-ttu-id="f5ef1-118">指定 Power BI 工作區集合的名稱。</span><span class="sxs-lookup"><span data-stu-id="f5ef1-118">Specifies a name for the Power BI workspace collection.</span></span>

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

### <span data-ttu-id="f5ef1-119">-確認</span><span class="sxs-lookup"><span data-stu-id="f5ef1-119">-Confirm</span></span>
<span data-ttu-id="f5ef1-120">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="f5ef1-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f5ef1-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f5ef1-121">-WhatIf</span></span>
<span data-ttu-id="f5ef1-122">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="f5ef1-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f5ef1-123">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f5ef1-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f5ef1-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5ef1-124">CommonParameters</span></span>
<span data-ttu-id="f5ef1-125">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="f5ef1-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5ef1-126">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="f5ef1-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5ef1-127">輸入</span><span class="sxs-lookup"><span data-stu-id="f5ef1-127">INPUTS</span></span>

### <span data-ttu-id="f5ef1-128">System.String</span><span class="sxs-lookup"><span data-stu-id="f5ef1-128">System.String</span></span>

## <span data-ttu-id="f5ef1-129">輸出</span><span class="sxs-lookup"><span data-stu-id="f5ef1-129">OUTPUTS</span></span>

### <span data-ttu-id="f5ef1-130">Microsoft.Azure.Commands.management.PowerBIEmbedded.models.PSWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="f5ef1-130">Microsoft.Azure.Commands.Management.PowerBIEmbedded.Models.PSWorkspaceCollection</span></span>

## <span data-ttu-id="f5ef1-131">筆記</span><span class="sxs-lookup"><span data-stu-id="f5ef1-131">NOTES</span></span>

## <span data-ttu-id="f5ef1-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="f5ef1-132">RELATED LINKS</span></span>

[<span data-ttu-id="f5ef1-133">Get-AzPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="f5ef1-133">Get-AzPowerBIWorkspaceCollection</span></span>](./Get-AzPowerBIWorkspaceCollection.md)

[<span data-ttu-id="f5ef1-134">Remove-AzPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="f5ef1-134">Remove-AzPowerBIWorkspaceCollection</span></span>](./Remove-AzPowerBIWorkspaceCollection.md)


