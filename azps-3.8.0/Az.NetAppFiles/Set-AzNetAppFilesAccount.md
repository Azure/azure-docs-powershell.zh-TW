---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/set-aznetappfilesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Set-AzNetAppFilesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Set-AzNetAppFilesAccount.md
ms.openlocfilehash: d2a379567ab96f5776b55c4cfbac2eabeaeb02a7
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93796681"
---
# <span data-ttu-id="7b874-101">Set-AzNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="7b874-101">Set-AzNetAppFilesAccount</span></span>

## <span data-ttu-id="7b874-102">摘要</span><span class="sxs-lookup"><span data-stu-id="7b874-102">SYNOPSIS</span></span>
<span data-ttu-id="7b874-103">使用新的資料集，更新 (ANF) 帳戶的 Azure NetApp 檔案。</span><span class="sxs-lookup"><span data-stu-id="7b874-103">Updates an Azure NetApp Files (ANF) account with the new data set.</span></span> <span data-ttu-id="7b874-104">對於刪除關聯的活動目錄很有用。</span><span class="sxs-lookup"><span data-stu-id="7b874-104">Useful for deletion of associated active directories.</span></span>

## <span data-ttu-id="7b874-105">句法</span><span class="sxs-lookup"><span data-stu-id="7b874-105">SYNTAX</span></span>

```
Set-AzNetAppFilesAccount -ResourceGroupName <String> -Location <String> -Name <String>
 [-ActiveDirectories <PSNetAppFilesActiveDirectory[]>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7b874-106">說明</span><span class="sxs-lookup"><span data-stu-id="7b874-106">DESCRIPTION</span></span>
<span data-ttu-id="7b874-107">**AzNetAppFilesAccount** Cmdlet 會修改 ANF 帳戶。</span><span class="sxs-lookup"><span data-stu-id="7b874-107">The **Set-AzNetAppFilesAccount** cmdlet modifies an ANF account.</span></span>

## <span data-ttu-id="7b874-108">示例</span><span class="sxs-lookup"><span data-stu-id="7b874-108">EXAMPLES</span></span>

### <span data-ttu-id="7b874-109">範例1：修改 ANF 帳戶</span><span class="sxs-lookup"><span data-stu-id="7b874-109">Example 1 : Modify an ANF account</span></span>
```
PS C:\>Set-AzNetAppFilesAccount -ResourceGroupName "MyRG" -l "westus2" -Name "MyAnfAccount"

Output:

Location          : westus2
Id                : /subscriptions/subsId/resourceGroups/MyRG/providers/Microsoft.NetApp/netAppAccounts/MyAnfAccount
Name              : MyAnfAccount
Type              : Microsoft.NetApp/netAppAccounts
Tags              :
AccountId         : 9fa2ca6d-1e48-4439-30e3-7de056e44e5a
ActiveDirectories : {}
ProvisioningState : Succeeded
```

<span data-ttu-id="7b874-110">這個命令會在指定的帳號上執行更新。</span><span class="sxs-lookup"><span data-stu-id="7b874-110">This command performs an update on the given account.</span></span> <span data-ttu-id="7b874-111">沒有 active directory 表示它將從帳戶中移除。</span><span class="sxs-lookup"><span data-stu-id="7b874-111">The absence of the active directory means it will be removed from the account.</span></span>

## <span data-ttu-id="7b874-112">參數</span><span class="sxs-lookup"><span data-stu-id="7b874-112">PARAMETERS</span></span>

### <span data-ttu-id="7b874-113">-ActiveDirectories</span><span class="sxs-lookup"><span data-stu-id="7b874-113">-ActiveDirectories</span></span>
<span data-ttu-id="7b874-114">代表活動目錄的 hashtable 陣列</span><span class="sxs-lookup"><span data-stu-id="7b874-114">A hashtable array which represents the active directories</span></span>

```yaml
Type: PSNetAppFilesActiveDirectory[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b874-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7b874-115">-DefaultProfile</span></span>
<span data-ttu-id="7b874-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="7b874-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b874-117">-位置</span><span class="sxs-lookup"><span data-stu-id="7b874-117">-Location</span></span>
<span data-ttu-id="7b874-118">資源的位置</span><span class="sxs-lookup"><span data-stu-id="7b874-118">The location of the resource</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b874-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="7b874-119">-Name</span></span>
<span data-ttu-id="7b874-120">ANF 帳戶的名稱</span><span class="sxs-lookup"><span data-stu-id="7b874-120">The name of the ANF account</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b874-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7b874-121">-ResourceGroupName</span></span>
<span data-ttu-id="7b874-122">ANF 帳戶的 [資源] 群組</span><span class="sxs-lookup"><span data-stu-id="7b874-122">The resource group of the ANF account</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b874-123">-Tag</span><span class="sxs-lookup"><span data-stu-id="7b874-123">-Tag</span></span>
<span data-ttu-id="7b874-124">代表資源標記的 hashtable</span><span class="sxs-lookup"><span data-stu-id="7b874-124">A hashtable which represents resource tags</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b874-125">-確認</span><span class="sxs-lookup"><span data-stu-id="7b874-125">-Confirm</span></span>
<span data-ttu-id="7b874-126">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="7b874-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b874-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7b874-127">-WhatIf</span></span>
<span data-ttu-id="7b874-128">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="7b874-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7b874-129">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="7b874-129">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b874-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b874-130">CommonParameters</span></span>
<span data-ttu-id="7b874-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="7b874-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="7b874-132">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="7b874-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b874-133">輸入</span><span class="sxs-lookup"><span data-stu-id="7b874-133">INPUTS</span></span>

### <span data-ttu-id="7b874-134">所有</span><span class="sxs-lookup"><span data-stu-id="7b874-134">None</span></span>

## <span data-ttu-id="7b874-135">輸出</span><span class="sxs-lookup"><span data-stu-id="7b874-135">OUTPUTS</span></span>

### <span data-ttu-id="7b874-136">PSNetAppFilesAccount 中的 NetAppFiles。</span><span class="sxs-lookup"><span data-stu-id="7b874-136">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="7b874-137">筆記</span><span class="sxs-lookup"><span data-stu-id="7b874-137">NOTES</span></span>

## <span data-ttu-id="7b874-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="7b874-138">RELATED LINKS</span></span>
