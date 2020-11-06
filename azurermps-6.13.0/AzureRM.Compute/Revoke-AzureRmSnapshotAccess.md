---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/revoke-azurermsnapshotaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Revoke-AzureRmSnapshotAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Revoke-AzureRmSnapshotAccess.md
ms.openlocfilehash: eb71d1a74e68bdf4157cacd4b87aa9a05bdc00db
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93443959"
---
# <span data-ttu-id="eaf56-101">Revoke-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="eaf56-101">Revoke-AzureRmSnapshotAccess</span></span>

## <span data-ttu-id="eaf56-102">摘要</span><span class="sxs-lookup"><span data-stu-id="eaf56-102">SYNOPSIS</span></span>
<span data-ttu-id="eaf56-103">吊銷快照存取權。</span><span class="sxs-lookup"><span data-stu-id="eaf56-103">Revokes an access to a snapshot.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="eaf56-104">句法</span><span class="sxs-lookup"><span data-stu-id="eaf56-104">SYNTAX</span></span>

```
Revoke-AzureRmSnapshotAccess [-ResourceGroupName] <String> [-SnapshotName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eaf56-105">說明</span><span class="sxs-lookup"><span data-stu-id="eaf56-105">DESCRIPTION</span></span>
<span data-ttu-id="eaf56-106">**Revoke AzureRmSnapshotAccess** Cmdlet 會吊銷快照的存取權。</span><span class="sxs-lookup"><span data-stu-id="eaf56-106">The **Revoke-AzureRmSnapshotAccess** cmdlet revokes an access to a snapshot.</span></span>

## <span data-ttu-id="eaf56-107">示例</span><span class="sxs-lookup"><span data-stu-id="eaf56-107">EXAMPLES</span></span>

### <span data-ttu-id="eaf56-108">範例1</span><span class="sxs-lookup"><span data-stu-id="eaf56-108">Example 1</span></span>
```
PS C:\> Revoke-AzureRmDiskAccess -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01'
```

<span data-ttu-id="eaf56-109">廢除名為「ResourceGroup01」的資源群組中名為「Snapshot01」的快照存取權</span><span class="sxs-lookup"><span data-stu-id="eaf56-109">Revoke the access to the snapshot named 'Snapshot01' in the resource group named 'ResourceGroup01'</span></span>

## <span data-ttu-id="eaf56-110">參數</span><span class="sxs-lookup"><span data-stu-id="eaf56-110">PARAMETERS</span></span>

### <span data-ttu-id="eaf56-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="eaf56-111">-AsJob</span></span>
<span data-ttu-id="eaf56-112">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="eaf56-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="eaf56-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eaf56-113">-DefaultProfile</span></span>
<span data-ttu-id="eaf56-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="eaf56-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="eaf56-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eaf56-115">-ResourceGroupName</span></span>
<span data-ttu-id="eaf56-116">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="eaf56-116">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eaf56-117">-SnapshotName</span><span class="sxs-lookup"><span data-stu-id="eaf56-117">-SnapshotName</span></span>
<span data-ttu-id="eaf56-118">指定快照的名稱。</span><span class="sxs-lookup"><span data-stu-id="eaf56-118">Specifies the name of a snapshot.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eaf56-119">-確認</span><span class="sxs-lookup"><span data-stu-id="eaf56-119">-Confirm</span></span>
<span data-ttu-id="eaf56-120">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="eaf56-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eaf56-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eaf56-121">-WhatIf</span></span>
<span data-ttu-id="eaf56-122">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="eaf56-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="eaf56-123">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="eaf56-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eaf56-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eaf56-124">CommonParameters</span></span>
<span data-ttu-id="eaf56-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="eaf56-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eaf56-126">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="eaf56-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eaf56-127">輸入</span><span class="sxs-lookup"><span data-stu-id="eaf56-127">INPUTS</span></span>

### <span data-ttu-id="eaf56-128">System.object</span><span class="sxs-lookup"><span data-stu-id="eaf56-128">System.String</span></span>

## <span data-ttu-id="eaf56-129">輸出</span><span class="sxs-lookup"><span data-stu-id="eaf56-129">OUTPUTS</span></span>

### <span data-ttu-id="eaf56-130">PSOperationStatusResponse 中的 [計算] 命令。</span><span class="sxs-lookup"><span data-stu-id="eaf56-130">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="eaf56-131">筆記</span><span class="sxs-lookup"><span data-stu-id="eaf56-131">NOTES</span></span>

## <span data-ttu-id="eaf56-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="eaf56-132">RELATED LINKS</span></span>
