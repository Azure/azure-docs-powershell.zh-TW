---
external help file: Microsoft.Azure.Commands.Management.PowerBIEmbedded.dll-Help.xml
Module Name: AzureRM.PowerBIEmbedded
ms.assetid: 9F9E4273-6747-4963-AF1F-C0AEB46770A4
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.Management.PowerBIEmbedded/help/New-AzureRmPowerBIWorkspaceCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.Management.PowerBIEmbedded/help/New-AzureRmPowerBIWorkspaceCollection.md
ms.openlocfilehash: 981daec060f47a88b31454cd8d13711091bedcf6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93455680"
---
# <span data-ttu-id="40aa3-101">New-AzureRmPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="40aa3-101">New-AzureRmPowerBIWorkspaceCollection</span></span>

## <span data-ttu-id="40aa3-102">摘要</span><span class="sxs-lookup"><span data-stu-id="40aa3-102">SYNOPSIS</span></span>
<span data-ttu-id="40aa3-103">建立 Power BI 工作區集合。</span><span class="sxs-lookup"><span data-stu-id="40aa3-103">Creates a Power BI workspace collection.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="40aa3-104">句法</span><span class="sxs-lookup"><span data-stu-id="40aa3-104">SYNTAX</span></span>

```
New-AzureRmPowerBIWorkspaceCollection [-ResourceGroupName] <String> [-WorkspaceCollectionName] <String>
 [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="40aa3-105">說明</span><span class="sxs-lookup"><span data-stu-id="40aa3-105">DESCRIPTION</span></span>
<span data-ttu-id="40aa3-106">**新的-AzureRmPowerBIWorkspaceCollection** Cmdlet 會在指定的資源群組和位置中為您的 Azure 訂閱建立 Power BI 工作區集合。</span><span class="sxs-lookup"><span data-stu-id="40aa3-106">The **New-AzureRmPowerBIWorkspaceCollection** cmdlet creates a Power BI workspace collection for your Azure subscription in the specified resource group and location.</span></span>

## <span data-ttu-id="40aa3-107">示例</span><span class="sxs-lookup"><span data-stu-id="40aa3-107">EXAMPLES</span></span>

### <span data-ttu-id="40aa3-108">範例1：建立工作區集合</span><span class="sxs-lookup"><span data-stu-id="40aa3-108">Example 1: Create a workspace collection</span></span>
```
PS C:\>New-AzureRmPowerBIWorkspaceCollection -ResourceGroupName "ResourceGroup17" -WorkspaceCollectionName "WCN11" -Location "Japan West"
```

<span data-ttu-id="40aa3-109">這個命令會在指定的資源群組的指定位置中，建立名為 WCN11 的工作區集合。</span><span class="sxs-lookup"><span data-stu-id="40aa3-109">This command creates a workspace collection named WCN11 in the specified resource group in the specified location.</span></span>

## <span data-ttu-id="40aa3-110">參數</span><span class="sxs-lookup"><span data-stu-id="40aa3-110">PARAMETERS</span></span>

### <span data-ttu-id="40aa3-111">-位置</span><span class="sxs-lookup"><span data-stu-id="40aa3-111">-Location</span></span>
<span data-ttu-id="40aa3-112">指定此 Cmdlet 建立工作區集合的 Azure 位置。</span><span class="sxs-lookup"><span data-stu-id="40aa3-112">Specifies the Azure location in which this cmdlet creates a workspace collection.</span></span>

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

### <span data-ttu-id="40aa3-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="40aa3-113">-ResourceGroupName</span></span>
<span data-ttu-id="40aa3-114">指定此 Cmdlet 建立工作區集合之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="40aa3-114">Specifies the name of the resource group in which this cmdlet creates a workspace collection.</span></span>

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

### <span data-ttu-id="40aa3-115">-WorkspaceCollectionName</span><span class="sxs-lookup"><span data-stu-id="40aa3-115">-WorkspaceCollectionName</span></span>
<span data-ttu-id="40aa3-116">指定 Power BI 工作區集合的名稱。</span><span class="sxs-lookup"><span data-stu-id="40aa3-116">Specifies a name for the Power BI workspace collection.</span></span>

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

### <span data-ttu-id="40aa3-117">-確認</span><span class="sxs-lookup"><span data-stu-id="40aa3-117">-Confirm</span></span>
<span data-ttu-id="40aa3-118">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="40aa3-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="40aa3-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="40aa3-119">-WhatIf</span></span>
<span data-ttu-id="40aa3-120">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="40aa3-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="40aa3-121">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="40aa3-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="40aa3-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40aa3-122">-DefaultProfile</span></span>
<span data-ttu-id="40aa3-123">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="40aa3-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40aa3-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40aa3-124">CommonParameters</span></span>
<span data-ttu-id="40aa3-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="40aa3-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40aa3-126">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="40aa3-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40aa3-127">輸入</span><span class="sxs-lookup"><span data-stu-id="40aa3-127">INPUTS</span></span>

## <span data-ttu-id="40aa3-128">輸出</span><span class="sxs-lookup"><span data-stu-id="40aa3-128">OUTPUTS</span></span>

### <span data-ttu-id="40aa3-129">PSWorkspaceCollection （PowerBIEmbedded.）。</span><span class="sxs-lookup"><span data-stu-id="40aa3-129">Microsoft.Azure.Commands.Management.PowerBIEmbedded.Models.PSWorkspaceCollection</span></span>

## <span data-ttu-id="40aa3-130">筆記</span><span class="sxs-lookup"><span data-stu-id="40aa3-130">NOTES</span></span>

## <span data-ttu-id="40aa3-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="40aa3-131">RELATED LINKS</span></span>

[<span data-ttu-id="40aa3-132">AzureRmPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="40aa3-132">Get-AzureRmPowerBIWorkspaceCollection</span></span>](./Get-AzureRmPowerBIWorkspaceCollection.md)

[<span data-ttu-id="40aa3-133">移除-AzureRmPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="40aa3-133">Remove-AzureRmPowerBIWorkspaceCollection</span></span>](./Remove-AzureRmPowerBIWorkspaceCollection.md)


