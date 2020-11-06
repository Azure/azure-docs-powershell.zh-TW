---
external help file: Microsoft.Azure.Commands.Management.PowerBIEmbedded.dll-Help.xml
Module Name: AzureRM.PowerBIEmbedded
ms.assetid: 9F9E4273-6747-4963-AF1F-C0AEB46770A4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.powerbiembedded/new-azurermpowerbiworkspacecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.Management.PowerBIEmbedded/help/New-AzureRmPowerBIWorkspaceCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.Management.PowerBIEmbedded/help/New-AzureRmPowerBIWorkspaceCollection.md
ms.openlocfilehash: 56cf34fce43465594a0a8862194bb15b117dda6a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93444488"
---
# <span data-ttu-id="bb326-101">New-AzureRmPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="bb326-101">New-AzureRmPowerBIWorkspaceCollection</span></span>

## <span data-ttu-id="bb326-102">摘要</span><span class="sxs-lookup"><span data-stu-id="bb326-102">SYNOPSIS</span></span>
<span data-ttu-id="bb326-103">建立 Power BI 工作區集合。</span><span class="sxs-lookup"><span data-stu-id="bb326-103">Creates a Power BI workspace collection.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bb326-104">句法</span><span class="sxs-lookup"><span data-stu-id="bb326-104">SYNTAX</span></span>

```
New-AzureRmPowerBIWorkspaceCollection [-ResourceGroupName] <String> [-WorkspaceCollectionName] <String>
 [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bb326-105">說明</span><span class="sxs-lookup"><span data-stu-id="bb326-105">DESCRIPTION</span></span>
<span data-ttu-id="bb326-106">**新的-AzureRmPowerBIWorkspaceCollection** Cmdlet 會在指定的資源群組和位置中為您的 Azure 訂閱建立 Power BI 工作區集合。</span><span class="sxs-lookup"><span data-stu-id="bb326-106">The **New-AzureRmPowerBIWorkspaceCollection** cmdlet creates a Power BI workspace collection for your Azure subscription in the specified resource group and location.</span></span>

## <span data-ttu-id="bb326-107">示例</span><span class="sxs-lookup"><span data-stu-id="bb326-107">EXAMPLES</span></span>

### <span data-ttu-id="bb326-108">範例1：建立工作區集合</span><span class="sxs-lookup"><span data-stu-id="bb326-108">Example 1: Create a workspace collection</span></span>
```
PS C:\>New-AzureRmPowerBIWorkspaceCollection -ResourceGroupName "ResourceGroup17" -WorkspaceCollectionName "WCN11" -Location "Japan West"
```

<span data-ttu-id="bb326-109">這個命令會在指定的資源群組的指定位置中，建立名為 WCN11 的工作區集合。</span><span class="sxs-lookup"><span data-stu-id="bb326-109">This command creates a workspace collection named WCN11 in the specified resource group in the specified location.</span></span>

## <span data-ttu-id="bb326-110">參數</span><span class="sxs-lookup"><span data-stu-id="bb326-110">PARAMETERS</span></span>

### <span data-ttu-id="bb326-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb326-111">-DefaultProfile</span></span>
<span data-ttu-id="bb326-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="bb326-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb326-113">-位置</span><span class="sxs-lookup"><span data-stu-id="bb326-113">-Location</span></span>
<span data-ttu-id="bb326-114">指定此 Cmdlet 建立工作區集合的 Azure 位置。</span><span class="sxs-lookup"><span data-stu-id="bb326-114">Specifies the Azure location in which this cmdlet creates a workspace collection.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bb326-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bb326-115">-ResourceGroupName</span></span>
<span data-ttu-id="bb326-116">指定此 Cmdlet 建立工作區集合之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="bb326-116">Specifies the name of the resource group in which this cmdlet creates a workspace collection.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bb326-117">-WorkspaceCollectionName</span><span class="sxs-lookup"><span data-stu-id="bb326-117">-WorkspaceCollectionName</span></span>
<span data-ttu-id="bb326-118">指定 Power BI 工作區集合的名稱。</span><span class="sxs-lookup"><span data-stu-id="bb326-118">Specifies a name for the Power BI workspace collection.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bb326-119">-確認</span><span class="sxs-lookup"><span data-stu-id="bb326-119">-Confirm</span></span>
<span data-ttu-id="bb326-120">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="bb326-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb326-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bb326-121">-WhatIf</span></span>
<span data-ttu-id="bb326-122">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="bb326-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bb326-123">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="bb326-123">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb326-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb326-124">CommonParameters</span></span>
<span data-ttu-id="bb326-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="bb326-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb326-126">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="bb326-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb326-127">輸入</span><span class="sxs-lookup"><span data-stu-id="bb326-127">INPUTS</span></span>

### <span data-ttu-id="bb326-128">所有</span><span class="sxs-lookup"><span data-stu-id="bb326-128">None</span></span>
<span data-ttu-id="bb326-129">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="bb326-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="bb326-130">輸出</span><span class="sxs-lookup"><span data-stu-id="bb326-130">OUTPUTS</span></span>

### <span data-ttu-id="bb326-131">PSWorkspaceCollection （PowerBIEmbedded.）。</span><span class="sxs-lookup"><span data-stu-id="bb326-131">Microsoft.Azure.Commands.Management.PowerBIEmbedded.Models.PSWorkspaceCollection</span></span>

## <span data-ttu-id="bb326-132">筆記</span><span class="sxs-lookup"><span data-stu-id="bb326-132">NOTES</span></span>

## <span data-ttu-id="bb326-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="bb326-133">RELATED LINKS</span></span>

[<span data-ttu-id="bb326-134">AzureRmPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="bb326-134">Get-AzureRmPowerBIWorkspaceCollection</span></span>](./Get-AzureRmPowerBIWorkspaceCollection.md)

[<span data-ttu-id="bb326-135">移除-AzureRmPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="bb326-135">Remove-AzureRmPowerBIWorkspaceCollection</span></span>](./Remove-AzureRmPowerBIWorkspaceCollection.md)


