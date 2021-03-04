---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PowerBIEmbedded.dll-Help.xml
Module Name: Az.PowerBIEmbedded
ms.assetid: 8FB2D9A0-BF7A-482D-B3A2-566FCA8C62A1
online version: https://docs.microsoft.com/powershell/module/az.powerbiembedded/reset-azpowerbiworkspacecollectionaccesskey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Reset-AzPowerBIWorkspaceCollectionAccessKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Reset-AzPowerBIWorkspaceCollectionAccessKey.md
ms.openlocfilehash: 2685013ed07eef18ed1b9ac78631c37acf52b205
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101902278"
---
# <span data-ttu-id="c718a-101">Reset-AzPowerBIWorkspaceCollectionAccessKey</span><span class="sxs-lookup"><span data-stu-id="c718a-101">Reset-AzPowerBIWorkspaceCollectionAccessKey</span></span>

## <span data-ttu-id="c718a-102">簡介</span><span class="sxs-lookup"><span data-stu-id="c718a-102">SYNOPSIS</span></span>
<span data-ttu-id="c718a-103">重設指定的便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="c718a-103">Resets the specified access key.</span></span>

## <span data-ttu-id="c718a-104">語法</span><span class="sxs-lookup"><span data-stu-id="c718a-104">SYNTAX</span></span>

```
Reset-AzPowerBIWorkspaceCollectionAccessKey [-ResourceGroupName] <String> [-WorkspaceCollectionName] <String>
 [-Key1] [-Key2] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c718a-105">描述</span><span class="sxs-lookup"><span data-stu-id="c718a-105">DESCRIPTION</span></span>
<span data-ttu-id="c718a-106">**Reset-AzPowerBIWorkspaceCollectionAccessKey** Cmdlet 會重設 Power BI 工作區集合中指定的便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="c718a-106">The **Reset-AzPowerBIWorkspaceCollectionAccessKey** cmdlet resets the specified access key in your Power BI workspace collection.</span></span>

## <span data-ttu-id="c718a-107">例子</span><span class="sxs-lookup"><span data-stu-id="c718a-107">EXAMPLES</span></span>

### <span data-ttu-id="c718a-108">範例 1：重設主便捷鍵</span><span class="sxs-lookup"><span data-stu-id="c718a-108">Example 1: Reset the primary access key</span></span>
```
PS C:\>Reset-AzPowerBIWorkspaceCollectionAccessKey -ResourceGroupName "ResourceGroup17" -WorkspaceCollectionName "WCN11" -Key1
```

<span data-ttu-id="c718a-109">此命令會重設指定資源群組中名為 WCN11 之工作區集合的主便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="c718a-109">This command resets the primary access key for the workspace collection named WCN11 in the specified resource group.</span></span>

## <span data-ttu-id="c718a-110">參數</span><span class="sxs-lookup"><span data-stu-id="c718a-110">PARAMETERS</span></span>

### <span data-ttu-id="c718a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c718a-111">-DefaultProfile</span></span>
<span data-ttu-id="c718a-112">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="c718a-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c718a-113">-Key1</span><span class="sxs-lookup"><span data-stu-id="c718a-113">-Key1</span></span>
<span data-ttu-id="c718a-114">表示此 Cmdlet 會重設主便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="c718a-114">Indicates that this cmdlet resets the primary access key.</span></span>

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

### <span data-ttu-id="c718a-115">-Key2</span><span class="sxs-lookup"><span data-stu-id="c718a-115">-Key2</span></span>
<span data-ttu-id="c718a-116">表示此 Cmdlet 會重設次要便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="c718a-116">Indicates that this cmdlet resets the secondary access key.</span></span>

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

### <span data-ttu-id="c718a-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c718a-117">-ResourceGroupName</span></span>
<span data-ttu-id="c718a-118">指定集合的資源組名。</span><span class="sxs-lookup"><span data-stu-id="c718a-118">Specifies the name of the resource group of the collection.</span></span>

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

### <span data-ttu-id="c718a-119">-WorkspaceCollectionName</span><span class="sxs-lookup"><span data-stu-id="c718a-119">-WorkspaceCollectionName</span></span>
<span data-ttu-id="c718a-120">指定此 Cmdlet 操作之 Power BI 工作區集合的名稱。</span><span class="sxs-lookup"><span data-stu-id="c718a-120">Specifies the name of the Power BI workspace collection on which this cmdlet operates.</span></span>

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

### <span data-ttu-id="c718a-121">-確認</span><span class="sxs-lookup"><span data-stu-id="c718a-121">-Confirm</span></span>
<span data-ttu-id="c718a-122">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="c718a-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c718a-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c718a-123">-WhatIf</span></span>
<span data-ttu-id="c718a-124">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="c718a-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c718a-125">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c718a-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c718a-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c718a-126">CommonParameters</span></span>
<span data-ttu-id="c718a-127">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="c718a-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c718a-128">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="c718a-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c718a-129">輸入</span><span class="sxs-lookup"><span data-stu-id="c718a-129">INPUTS</span></span>

### <span data-ttu-id="c718a-130">System.String</span><span class="sxs-lookup"><span data-stu-id="c718a-130">System.String</span></span>

## <span data-ttu-id="c718a-131">輸出</span><span class="sxs-lookup"><span data-stu-id="c718a-131">OUTPUTS</span></span>

### <span data-ttu-id="c718a-132">Microsoft.Azure.Commands.management.PowerBIEmbedded.models.PSWorkspaceCollectionAccessKey</span><span class="sxs-lookup"><span data-stu-id="c718a-132">Microsoft.Azure.Commands.Management.PowerBIEmbedded.Models.PSWorkspaceCollectionAccessKey</span></span>

## <span data-ttu-id="c718a-133">筆記</span><span class="sxs-lookup"><span data-stu-id="c718a-133">NOTES</span></span>

## <span data-ttu-id="c718a-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="c718a-134">RELATED LINKS</span></span>

[<span data-ttu-id="c718a-135">Get-AzPowerBIWorkspaceCollectionAccessKey</span><span class="sxs-lookup"><span data-stu-id="c718a-135">Get-AzPowerBIWorkspaceCollectionAccessKey</span></span>](./Get-AzPowerBIWorkspaceCollectionAccessKey.md)


