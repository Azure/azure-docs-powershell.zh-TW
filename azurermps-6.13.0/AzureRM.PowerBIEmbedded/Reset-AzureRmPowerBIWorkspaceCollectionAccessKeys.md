---
external help file: Microsoft.Azure.Commands.Management.PowerBIEmbedded.dll-Help.xml
Module Name: AzureRM.PowerBIEmbedded
ms.assetid: 8FB2D9A0-BF7A-482D-B3A2-566FCA8C62A1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.powerbiembedded/reset-azurermpowerbiworkspacecollectionaccesskeys
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.Management.PowerBIEmbedded/help/Reset-AzureRmPowerBIWorkspaceCollectionAccessKeys.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.Management.PowerBIEmbedded/help/Reset-AzureRmPowerBIWorkspaceCollectionAccessKeys.md
ms.openlocfilehash: cb8236acfc0fd1d349091593a2510da271820020
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93626049"
---
# <span data-ttu-id="24df8-101">Reset-AzureRmPowerBIWorkspaceCollectionAccessKeys</span><span class="sxs-lookup"><span data-stu-id="24df8-101">Reset-AzureRmPowerBIWorkspaceCollectionAccessKeys</span></span>

## <span data-ttu-id="24df8-102">摘要</span><span class="sxs-lookup"><span data-stu-id="24df8-102">SYNOPSIS</span></span>
<span data-ttu-id="24df8-103">重設指定的便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="24df8-103">Resets the specified access key.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="24df8-104">句法</span><span class="sxs-lookup"><span data-stu-id="24df8-104">SYNTAX</span></span>

```
Reset-AzureRmPowerBIWorkspaceCollectionAccessKeys [-ResourceGroupName] <String>
 [-WorkspaceCollectionName] <String> [-Key1] [-Key2] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="24df8-105">說明</span><span class="sxs-lookup"><span data-stu-id="24df8-105">DESCRIPTION</span></span>
<span data-ttu-id="24df8-106">**Reset AzureRmPowerBIWorkspaceCollectionAccessKeys** Cmdlet 會在 Power BI 工作區集合中重設指定的便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="24df8-106">The **Reset-AzureRmPowerBIWorkspaceCollectionAccessKeys** cmdlet resets the specified access key in your Power BI workspace collection.</span></span>

## <span data-ttu-id="24df8-107">示例</span><span class="sxs-lookup"><span data-stu-id="24df8-107">EXAMPLES</span></span>

### <span data-ttu-id="24df8-108">範例1：重設主要便捷鍵</span><span class="sxs-lookup"><span data-stu-id="24df8-108">Example 1: Reset the primary access key</span></span>
```
PS C:\>Reset-AzureRmPowerBIWorkspaceCollectionAccessKeys -ResourceGroupName "ResourceGroup17" -WorkspaceCollectionName "WCN11" -Key1
```

<span data-ttu-id="24df8-109">這個命令會在指定的資源群組中，重設名為 WCN11 的工作區集合的主要便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="24df8-109">This command resets the primary access key for the workspace collection named WCN11 in the specified resource group.</span></span>

## <span data-ttu-id="24df8-110">參數</span><span class="sxs-lookup"><span data-stu-id="24df8-110">PARAMETERS</span></span>

### <span data-ttu-id="24df8-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24df8-111">-DefaultProfile</span></span>
<span data-ttu-id="24df8-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="24df8-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="24df8-113">-Key1</span><span class="sxs-lookup"><span data-stu-id="24df8-113">-Key1</span></span>
<span data-ttu-id="24df8-114">表示此 Cmdlet 會重設主要便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="24df8-114">Indicates that this cmdlet resets the primary access key.</span></span>

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

### <span data-ttu-id="24df8-115">-Key2</span><span class="sxs-lookup"><span data-stu-id="24df8-115">-Key2</span></span>
<span data-ttu-id="24df8-116">表示此 Cmdlet 會重設副訪問金鑰。</span><span class="sxs-lookup"><span data-stu-id="24df8-116">Indicates that this cmdlet resets the secondary access key.</span></span>

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

### <span data-ttu-id="24df8-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="24df8-117">-ResourceGroupName</span></span>
<span data-ttu-id="24df8-118">指定集合之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="24df8-118">Specifies the name of the resource group of the collection.</span></span>

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

### <span data-ttu-id="24df8-119">-WorkspaceCollectionName</span><span class="sxs-lookup"><span data-stu-id="24df8-119">-WorkspaceCollectionName</span></span>
<span data-ttu-id="24df8-120">指定此 Cmdlet 在其上執行的 Power BI 工作區集合的名稱。</span><span class="sxs-lookup"><span data-stu-id="24df8-120">Specifies the name of the Power BI workspace collection on which this cmdlet operates.</span></span>

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

### <span data-ttu-id="24df8-121">-確認</span><span class="sxs-lookup"><span data-stu-id="24df8-121">-Confirm</span></span>
<span data-ttu-id="24df8-122">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="24df8-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="24df8-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="24df8-123">-WhatIf</span></span>
<span data-ttu-id="24df8-124">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="24df8-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="24df8-125">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="24df8-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="24df8-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24df8-126">CommonParameters</span></span>
<span data-ttu-id="24df8-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="24df8-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24df8-128">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="24df8-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24df8-129">輸入</span><span class="sxs-lookup"><span data-stu-id="24df8-129">INPUTS</span></span>

### <span data-ttu-id="24df8-130">System.object</span><span class="sxs-lookup"><span data-stu-id="24df8-130">System.String</span></span>

## <span data-ttu-id="24df8-131">輸出</span><span class="sxs-lookup"><span data-stu-id="24df8-131">OUTPUTS</span></span>

### <span data-ttu-id="24df8-132">PSWorkspaceCollectionAccessKey （PowerBIEmbedded.）。</span><span class="sxs-lookup"><span data-stu-id="24df8-132">Microsoft.Azure.Commands.Management.PowerBIEmbedded.Models.PSWorkspaceCollectionAccessKey</span></span>

## <span data-ttu-id="24df8-133">筆記</span><span class="sxs-lookup"><span data-stu-id="24df8-133">NOTES</span></span>

## <span data-ttu-id="24df8-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="24df8-134">RELATED LINKS</span></span>

[<span data-ttu-id="24df8-135">AzureRmPowerBIWorkspaceCollectionAccessKeys</span><span class="sxs-lookup"><span data-stu-id="24df8-135">Get-AzureRmPowerBIWorkspaceCollectionAccessKeys</span></span>](./Get-AzureRmPowerBIWorkspaceCollectionAccessKeys.md)


