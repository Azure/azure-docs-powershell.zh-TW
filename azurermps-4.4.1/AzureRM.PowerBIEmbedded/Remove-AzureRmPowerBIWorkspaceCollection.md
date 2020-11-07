---
external help file: Microsoft.Azure.Commands.Management.PowerBIEmbedded.dll-Help.xml
Module Name: AzureRM.PowerBIEmbedded
ms.assetid: 2D63CC6D-AB02-4299-A922-4057D6F595D7
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.Management.PowerBIEmbedded/help/Remove-AzureRmPowerBIWorkspaceCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.Management.PowerBIEmbedded/help/Remove-AzureRmPowerBIWorkspaceCollection.md
ms.openlocfilehash: c377beb022b3d44d8b96a560c4bdd8b0c6daa387
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93625988"
---
# <span data-ttu-id="ab894-101">Remove-AzureRmPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="ab894-101">Remove-AzureRmPowerBIWorkspaceCollection</span></span>

## <span data-ttu-id="ab894-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ab894-102">SYNOPSIS</span></span>
<span data-ttu-id="ab894-103">移除 Power BI 工作區集合。</span><span class="sxs-lookup"><span data-stu-id="ab894-103">Removes a Power BI workspace collection.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ab894-104">句法</span><span class="sxs-lookup"><span data-stu-id="ab894-104">SYNTAX</span></span>

```
Remove-AzureRmPowerBIWorkspaceCollection [-ResourceGroupName] <String> [-WorkspaceCollectionName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ab894-105">說明</span><span class="sxs-lookup"><span data-stu-id="ab894-105">DESCRIPTION</span></span>
<span data-ttu-id="ab894-106">**AzureRmPowerBIWorkspaceCollection** Cmdlet 會從您的 Azure 訂閱和資源群組中移除 Power BI 工作區集合。</span><span class="sxs-lookup"><span data-stu-id="ab894-106">The **Remove-AzureRmPowerBIWorkspaceCollection** cmdlet removes a Power BI workspace collection from your Azure subscription and resource group.</span></span>

## <span data-ttu-id="ab894-107">示例</span><span class="sxs-lookup"><span data-stu-id="ab894-107">EXAMPLES</span></span>

### <span data-ttu-id="ab894-108">範例1：移除工作區集合</span><span class="sxs-lookup"><span data-stu-id="ab894-108">Example 1: Remove a workspace collection</span></span>
```
PS C:\>Remove-AzureRmPowerBIWorkspaceCollection -ResourceGroupName "ResourceGroup17" -WorkspaceCollectionName "WCN11"
```

<span data-ttu-id="ab894-109">這個命令會從指定的資源群組中移除名為 WCN11 的工作區集合。</span><span class="sxs-lookup"><span data-stu-id="ab894-109">This command removes the workspace collection named WCN11 in the specified resource group.</span></span>

## <span data-ttu-id="ab894-110">參數</span><span class="sxs-lookup"><span data-stu-id="ab894-110">PARAMETERS</span></span>

### <span data-ttu-id="ab894-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ab894-111">-ResourceGroupName</span></span>
<span data-ttu-id="ab894-112">指定此 Cmdlet 從中移除工作區集合之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="ab894-112">Specifies the name of the resource group from which this cmdlet removes a workspace collection.</span></span>

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

### <span data-ttu-id="ab894-113">-WorkspaceCollectionName</span><span class="sxs-lookup"><span data-stu-id="ab894-113">-WorkspaceCollectionName</span></span>
<span data-ttu-id="ab894-114">指定此 Cmdlet 移除的 Power BI workspace 集合的名稱。</span><span class="sxs-lookup"><span data-stu-id="ab894-114">Specifies the name of the Power BI workspace collection that this cmdlet removes.</span></span>

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

### <span data-ttu-id="ab894-115">-確認</span><span class="sxs-lookup"><span data-stu-id="ab894-115">-Confirm</span></span>
<span data-ttu-id="ab894-116">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="ab894-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ab894-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ab894-117">-WhatIf</span></span>
<span data-ttu-id="ab894-118">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ab894-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ab894-119">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ab894-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ab894-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab894-120">-DefaultProfile</span></span>
<span data-ttu-id="ab894-121">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="ab894-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ab894-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab894-122">CommonParameters</span></span>
<span data-ttu-id="ab894-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ab894-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab894-124">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="ab894-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab894-125">輸入</span><span class="sxs-lookup"><span data-stu-id="ab894-125">INPUTS</span></span>

## <span data-ttu-id="ab894-126">輸出</span><span class="sxs-lookup"><span data-stu-id="ab894-126">OUTPUTS</span></span>

## <span data-ttu-id="ab894-127">筆記</span><span class="sxs-lookup"><span data-stu-id="ab894-127">NOTES</span></span>

## <span data-ttu-id="ab894-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="ab894-128">RELATED LINKS</span></span>

[<span data-ttu-id="ab894-129">AzureRmPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="ab894-129">Get-AzureRmPowerBIWorkspaceCollection</span></span>](./Get-AzureRmPowerBIWorkspaceCollection.md)

[<span data-ttu-id="ab894-130">新-AzureRmPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="ab894-130">New-AzureRmPowerBIWorkspaceCollection</span></span>](./New-AzureRmPowerBIWorkspaceCollection.md)


