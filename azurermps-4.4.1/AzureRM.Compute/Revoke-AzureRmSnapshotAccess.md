---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Revoke-AzureRmSnapshotAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Revoke-AzureRmSnapshotAccess.md
ms.openlocfilehash: 6d7b41ae7250a294b86333ecf2926a2eda06d3bb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93623510"
---
# <span data-ttu-id="81b7f-101">Revoke-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="81b7f-101">Revoke-AzureRmSnapshotAccess</span></span>

## <span data-ttu-id="81b7f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="81b7f-102">SYNOPSIS</span></span>
<span data-ttu-id="81b7f-103">吊銷快照存取權。</span><span class="sxs-lookup"><span data-stu-id="81b7f-103">Revokes an access to a snapshot.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="81b7f-104">句法</span><span class="sxs-lookup"><span data-stu-id="81b7f-104">SYNTAX</span></span>

```
Revoke-AzureRmSnapshotAccess [-ResourceGroupName] <String> [-SnapshotName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="81b7f-105">說明</span><span class="sxs-lookup"><span data-stu-id="81b7f-105">DESCRIPTION</span></span>
<span data-ttu-id="81b7f-106">**Revoke AzureRmSnapshotAccess** Cmdlet 會吊銷快照的存取權。</span><span class="sxs-lookup"><span data-stu-id="81b7f-106">The **Revoke-AzureRmSnapshotAccess** cmdlet revokes an access to a snapshot.</span></span>

## <span data-ttu-id="81b7f-107">示例</span><span class="sxs-lookup"><span data-stu-id="81b7f-107">EXAMPLES</span></span>

### <span data-ttu-id="81b7f-108">範例1</span><span class="sxs-lookup"><span data-stu-id="81b7f-108">Example 1</span></span>
```
PS C:\> Revoke-AzureRmDiskAccess -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01'
```

<span data-ttu-id="81b7f-109">廢除名為「ResourceGroup01」的資源群組中名為「Snapshot01」的快照存取權</span><span class="sxs-lookup"><span data-stu-id="81b7f-109">Revoke the access to the snapshot named 'Snapshot01' in the resource group named 'ResourceGroup01'</span></span>

## <span data-ttu-id="81b7f-110">參數</span><span class="sxs-lookup"><span data-stu-id="81b7f-110">PARAMETERS</span></span>

### <span data-ttu-id="81b7f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81b7f-111">-DefaultProfile</span></span>
<span data-ttu-id="81b7f-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="81b7f-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="81b7f-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="81b7f-113">-ResourceGroupName</span></span>
<span data-ttu-id="81b7f-114">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="81b7f-114">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="81b7f-115">-SnapshotName</span><span class="sxs-lookup"><span data-stu-id="81b7f-115">-SnapshotName</span></span>
<span data-ttu-id="81b7f-116">指定快照的名稱。</span><span class="sxs-lookup"><span data-stu-id="81b7f-116">Specifies the name of a snapshot.</span></span>

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

### <span data-ttu-id="81b7f-117">-確認</span><span class="sxs-lookup"><span data-stu-id="81b7f-117">-Confirm</span></span>
<span data-ttu-id="81b7f-118">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="81b7f-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="81b7f-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="81b7f-119">-WhatIf</span></span>
<span data-ttu-id="81b7f-120">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="81b7f-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="81b7f-121">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="81b7f-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="81b7f-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81b7f-122">CommonParameters</span></span>
<span data-ttu-id="81b7f-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="81b7f-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81b7f-124">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="81b7f-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81b7f-125">輸入</span><span class="sxs-lookup"><span data-stu-id="81b7f-125">INPUTS</span></span>

### <span data-ttu-id="81b7f-126">System.object</span><span class="sxs-lookup"><span data-stu-id="81b7f-126">System.String</span></span>

## <span data-ttu-id="81b7f-127">輸出</span><span class="sxs-lookup"><span data-stu-id="81b7f-127">OUTPUTS</span></span>

### <span data-ttu-id="81b7f-128">System.object</span><span class="sxs-lookup"><span data-stu-id="81b7f-128">System.Object</span></span>

## <span data-ttu-id="81b7f-129">筆記</span><span class="sxs-lookup"><span data-stu-id="81b7f-129">NOTES</span></span>

## <span data-ttu-id="81b7f-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="81b7f-130">RELATED LINKS</span></span>

