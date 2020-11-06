---
external help file: Microsoft.Azure.Commands.Management.PowerBIEmbedded.dll-Help.xml
Module Name: AzureRM.PowerBIEmbedded
ms.assetid: 8FB2D9A0-BF7A-482D-B3A2-566FCA8C62A1
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.Management.PowerBIEmbedded/help/Reset-AzureRmPowerBIWorkspaceCollectionAccessKeys.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.Management.PowerBIEmbedded/help/Reset-AzureRmPowerBIWorkspaceCollectionAccessKeys.md
ms.openlocfilehash: 766682df23beaa7c513ff54554a3ebd59a6d1537
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93455671"
---
# <span data-ttu-id="76194-101">Reset-AzureRmPowerBIWorkspaceCollectionAccessKeys</span><span class="sxs-lookup"><span data-stu-id="76194-101">Reset-AzureRmPowerBIWorkspaceCollectionAccessKeys</span></span>

## <span data-ttu-id="76194-102">摘要</span><span class="sxs-lookup"><span data-stu-id="76194-102">SYNOPSIS</span></span>
<span data-ttu-id="76194-103">重設指定的便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="76194-103">Resets the specified access key.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="76194-104">句法</span><span class="sxs-lookup"><span data-stu-id="76194-104">SYNTAX</span></span>

```
Reset-AzureRmPowerBIWorkspaceCollectionAccessKeys [-ResourceGroupName] <String>
 [-WorkspaceCollectionName] <String> [-Key1] [-Key2] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="76194-105">說明</span><span class="sxs-lookup"><span data-stu-id="76194-105">DESCRIPTION</span></span>
<span data-ttu-id="76194-106">**Reset AzureRmPowerBIWorkspaceCollectionAccessKeys** Cmdlet 會在 Power BI 工作區集合中重設指定的便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="76194-106">The **Reset-AzureRmPowerBIWorkspaceCollectionAccessKeys** cmdlet resets the specified access key in your Power BI workspace collection.</span></span>

## <span data-ttu-id="76194-107">示例</span><span class="sxs-lookup"><span data-stu-id="76194-107">EXAMPLES</span></span>

### <span data-ttu-id="76194-108">範例1：重設主要便捷鍵</span><span class="sxs-lookup"><span data-stu-id="76194-108">Example 1: Reset the primary access key</span></span>
```
PS C:\>Reset-AzureRmPowerBIWorkspaceCollectionAccessKeys -ResourceGroupName "ResourceGroup17" -WorkspaceCollectionName "WCN11" -Key1
```

<span data-ttu-id="76194-109">這個命令會在指定的資源群組中，重設名為 WCN11 的工作區集合的主要便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="76194-109">This command resets the primary access key for the workspace collection named WCN11 in the specified resource group.</span></span>

## <span data-ttu-id="76194-110">參數</span><span class="sxs-lookup"><span data-stu-id="76194-110">PARAMETERS</span></span>

### <span data-ttu-id="76194-111">-Key1</span><span class="sxs-lookup"><span data-stu-id="76194-111">-Key1</span></span>
<span data-ttu-id="76194-112">表示此 Cmdlet 會重設主要便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="76194-112">Indicates that this cmdlet resets the primary access key.</span></span>

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

### <span data-ttu-id="76194-113">-Key2</span><span class="sxs-lookup"><span data-stu-id="76194-113">-Key2</span></span>
<span data-ttu-id="76194-114">表示此 Cmdlet 會重設副訪問金鑰。</span><span class="sxs-lookup"><span data-stu-id="76194-114">Indicates that this cmdlet resets the secondary access key.</span></span>

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

### <span data-ttu-id="76194-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="76194-115">-ResourceGroupName</span></span>
<span data-ttu-id="76194-116">指定集合之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="76194-116">Specifies the name of the resource group of the collection.</span></span>

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

### <span data-ttu-id="76194-117">-WorkspaceCollectionName</span><span class="sxs-lookup"><span data-stu-id="76194-117">-WorkspaceCollectionName</span></span>
<span data-ttu-id="76194-118">指定此 Cmdlet 在其上執行的 Power BI 工作區集合的名稱。</span><span class="sxs-lookup"><span data-stu-id="76194-118">Specifies the name of the Power BI workspace collection on which this cmdlet operates.</span></span>

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

### <span data-ttu-id="76194-119">-確認</span><span class="sxs-lookup"><span data-stu-id="76194-119">-Confirm</span></span>
<span data-ttu-id="76194-120">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="76194-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="76194-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="76194-121">-WhatIf</span></span>
<span data-ttu-id="76194-122">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="76194-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="76194-123">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="76194-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="76194-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76194-124">-DefaultProfile</span></span>
<span data-ttu-id="76194-125">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="76194-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="76194-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76194-126">CommonParameters</span></span>
<span data-ttu-id="76194-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="76194-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76194-128">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="76194-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76194-129">輸入</span><span class="sxs-lookup"><span data-stu-id="76194-129">INPUTS</span></span>

## <span data-ttu-id="76194-130">輸出</span><span class="sxs-lookup"><span data-stu-id="76194-130">OUTPUTS</span></span>

### <span data-ttu-id="76194-131">PSWorkspaceCollectionAccessKey （PowerBIEmbedded.）。</span><span class="sxs-lookup"><span data-stu-id="76194-131">Microsoft.Azure.Commands.Management.PowerBIEmbedded.Models.PSWorkspaceCollectionAccessKey</span></span>

## <span data-ttu-id="76194-132">筆記</span><span class="sxs-lookup"><span data-stu-id="76194-132">NOTES</span></span>

## <span data-ttu-id="76194-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="76194-133">RELATED LINKS</span></span>

[<span data-ttu-id="76194-134">AzureRmPowerBIWorkspaceCollectionAccessKeys</span><span class="sxs-lookup"><span data-stu-id="76194-134">Get-AzureRmPowerBIWorkspaceCollectionAccessKeys</span></span>](./Get-AzureRmPowerBIWorkspaceCollectionAccessKeys.md)


