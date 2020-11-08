---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PowerBIEmbedded.dll-Help.xml
Module Name: Az.PowerBIEmbedded
ms.assetid: 8FB2D9A0-BF7A-482D-B3A2-566FCA8C62A1
online version: https://docs.microsoft.com/en-us/powershell/module/az.powerbiembedded/reset-azpowerbiworkspacecollectionaccesskey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Reset-AzPowerBIWorkspaceCollectionAccessKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Reset-AzPowerBIWorkspaceCollectionAccessKey.md
ms.openlocfilehash: d9e30c81eb0e2422b91be79bcfc7c732291c30cb
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94128860"
---
# <span data-ttu-id="90c87-101">Reset-AzPowerBIWorkspaceCollectionAccessKey</span><span class="sxs-lookup"><span data-stu-id="90c87-101">Reset-AzPowerBIWorkspaceCollectionAccessKey</span></span>

## <span data-ttu-id="90c87-102">摘要</span><span class="sxs-lookup"><span data-stu-id="90c87-102">SYNOPSIS</span></span>
<span data-ttu-id="90c87-103">重設指定的便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="90c87-103">Resets the specified access key.</span></span>

## <span data-ttu-id="90c87-104">句法</span><span class="sxs-lookup"><span data-stu-id="90c87-104">SYNTAX</span></span>

```
Reset-AzPowerBIWorkspaceCollectionAccessKey [-ResourceGroupName] <String> [-WorkspaceCollectionName] <String>
 [-Key1] [-Key2] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="90c87-105">說明</span><span class="sxs-lookup"><span data-stu-id="90c87-105">DESCRIPTION</span></span>
<span data-ttu-id="90c87-106">**Reset AzPowerBIWorkspaceCollectionAccessKey** Cmdlet 會在 Power BI 工作區集合中重設指定的便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="90c87-106">The **Reset-AzPowerBIWorkspaceCollectionAccessKey** cmdlet resets the specified access key in your Power BI workspace collection.</span></span>

## <span data-ttu-id="90c87-107">示例</span><span class="sxs-lookup"><span data-stu-id="90c87-107">EXAMPLES</span></span>

### <span data-ttu-id="90c87-108">範例1：重設主要便捷鍵</span><span class="sxs-lookup"><span data-stu-id="90c87-108">Example 1: Reset the primary access key</span></span>
```
PS C:\>Reset-AzPowerBIWorkspaceCollectionAccessKey -ResourceGroupName "ResourceGroup17" -WorkspaceCollectionName "WCN11" -Key1
```

<span data-ttu-id="90c87-109">這個命令會在指定的資源群組中，重設名為 WCN11 的工作區集合的主要便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="90c87-109">This command resets the primary access key for the workspace collection named WCN11 in the specified resource group.</span></span>

## <span data-ttu-id="90c87-110">參數</span><span class="sxs-lookup"><span data-stu-id="90c87-110">PARAMETERS</span></span>

### <span data-ttu-id="90c87-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90c87-111">-DefaultProfile</span></span>
<span data-ttu-id="90c87-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="90c87-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="90c87-113">-Key1</span><span class="sxs-lookup"><span data-stu-id="90c87-113">-Key1</span></span>
<span data-ttu-id="90c87-114">表示此 Cmdlet 會重設主要便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="90c87-114">Indicates that this cmdlet resets the primary access key.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90c87-115">-Key2</span><span class="sxs-lookup"><span data-stu-id="90c87-115">-Key2</span></span>
<span data-ttu-id="90c87-116">表示此 Cmdlet 會重設副訪問金鑰。</span><span class="sxs-lookup"><span data-stu-id="90c87-116">Indicates that this cmdlet resets the secondary access key.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90c87-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="90c87-117">-ResourceGroupName</span></span>
<span data-ttu-id="90c87-118">指定集合之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="90c87-118">Specifies the name of the resource group of the collection.</span></span>

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

### <span data-ttu-id="90c87-119">-WorkspaceCollectionName</span><span class="sxs-lookup"><span data-stu-id="90c87-119">-WorkspaceCollectionName</span></span>
<span data-ttu-id="90c87-120">指定此 Cmdlet 在其上執行的 Power BI 工作區集合的名稱。</span><span class="sxs-lookup"><span data-stu-id="90c87-120">Specifies the name of the Power BI workspace collection on which this cmdlet operates.</span></span>

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

### <span data-ttu-id="90c87-121">-確認</span><span class="sxs-lookup"><span data-stu-id="90c87-121">-Confirm</span></span>
<span data-ttu-id="90c87-122">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="90c87-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="90c87-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="90c87-123">-WhatIf</span></span>
<span data-ttu-id="90c87-124">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="90c87-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="90c87-125">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="90c87-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="90c87-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90c87-126">CommonParameters</span></span>
<span data-ttu-id="90c87-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="90c87-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90c87-128">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="90c87-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90c87-129">輸入</span><span class="sxs-lookup"><span data-stu-id="90c87-129">INPUTS</span></span>

### <span data-ttu-id="90c87-130">System.object</span><span class="sxs-lookup"><span data-stu-id="90c87-130">System.String</span></span>

## <span data-ttu-id="90c87-131">輸出</span><span class="sxs-lookup"><span data-stu-id="90c87-131">OUTPUTS</span></span>

### <span data-ttu-id="90c87-132">PSWorkspaceCollectionAccessKey （PowerBIEmbedded.）。</span><span class="sxs-lookup"><span data-stu-id="90c87-132">Microsoft.Azure.Commands.Management.PowerBIEmbedded.Models.PSWorkspaceCollectionAccessKey</span></span>

## <span data-ttu-id="90c87-133">筆記</span><span class="sxs-lookup"><span data-stu-id="90c87-133">NOTES</span></span>

## <span data-ttu-id="90c87-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="90c87-134">RELATED LINKS</span></span>

[<span data-ttu-id="90c87-135">AzPowerBIWorkspaceCollectionAccessKey</span><span class="sxs-lookup"><span data-stu-id="90c87-135">Get-AzPowerBIWorkspaceCollectionAccessKey</span></span>](./Get-AzPowerBIWorkspaceCollectionAccessKey.md)

