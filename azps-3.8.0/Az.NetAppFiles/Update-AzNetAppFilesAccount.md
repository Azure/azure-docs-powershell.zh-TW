---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/update-aznetappfilesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesAccount.md
ms.openlocfilehash: e6fa7a00218e52eae6b0323bc5e8ac25459986ce
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93796678"
---
# <span data-ttu-id="99f37-101">Update-AzNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="99f37-101">Update-AzNetAppFilesAccount</span></span>

## <span data-ttu-id="99f37-102">摘要</span><span class="sxs-lookup"><span data-stu-id="99f37-102">SYNOPSIS</span></span>
<span data-ttu-id="99f37-103">根據提供的選擇性修飾符，更新 (ANF) 帳戶的 Azure NetApp 檔案。</span><span class="sxs-lookup"><span data-stu-id="99f37-103">Updates an Azure NetApp Files (ANF) account according to the optional modifiers provided.</span></span>

## <span data-ttu-id="99f37-104">句法</span><span class="sxs-lookup"><span data-stu-id="99f37-104">SYNTAX</span></span>

```
Update-AzNetAppFilesAccount -ResourceGroupName <String> -Name <String> [-Location <String>]
 [-ActiveDirectories <PSNetAppFilesActiveDirectory[]>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```
### <span data-ttu-id="99f37-105">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="99f37-105">ByParentObjectParameterSet</span></span>
```
Update-AzNetAppFilesPool -Name <String> [-PoolSize <Int64>] [-ServiceLevel <String>] [-Tag <Hashtable>]
 -AccountObject <PSNetAppFilesAccount> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="99f37-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="99f37-106">ByResourceIdParameterSet</span></span>
```
Update-AzNetAppFilesPool [-PoolSize <Int64>] [-ServiceLevel <String>] [-Tag <Hashtable>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="99f37-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="99f37-107">ByObjectParameterSet</span></span>
```
Update-AzNetAppFilesPool [-PoolSize <Int64>] [-ServiceLevel <String>] [-Tag <Hashtable>]
 -InputObject <PSNetAppFilesPool> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="99f37-108">說明</span><span class="sxs-lookup"><span data-stu-id="99f37-108">DESCRIPTION</span></span>
<span data-ttu-id="99f37-109">**AzNetAppFilesAccount** Cmdlet 會修改 ANF 帳戶。</span><span class="sxs-lookup"><span data-stu-id="99f37-109">The **Update-AzNetAppFilesAccount** cmdlet modifies an ANF account.</span></span>

## <span data-ttu-id="99f37-110">示例</span><span class="sxs-lookup"><span data-stu-id="99f37-110">EXAMPLES</span></span>

### <span data-ttu-id="99f37-111">範例1：更新 ANF 帳戶</span><span class="sxs-lookup"><span data-stu-id="99f37-111">Example 1 : Updates an ANF account</span></span>
```
PS C:\>Update-AzNetAppFilesAccount -ResourceGroupName "MyRG" -l "westus2" -Name "MyAnfAccount" -Tag @{'Tag1' = 'Value1'}

Output:

Location          : westus2
Id                : /subscriptions/subsId/resourceGroups/MyRG/providers/Microsoft.NetApp/netAppAccounts/MyAnfAccount
Name              : MyAnfAccount
Type              : Microsoft.NetApp/netAppAccounts
Tags              : {Tag1}
AccountId         : 9fa2ca6d-1e48-4439-30e3-7de056e44e5a
ActiveDirectories :
ProvisioningState : Succeeded
```

<span data-ttu-id="99f37-112">這個命令會針對指定的帳號執行更新，將標籤修改為提供的標記。</span><span class="sxs-lookup"><span data-stu-id="99f37-112">This command performs an update on the given account modifying the tags to those provided.</span></span>

## <span data-ttu-id="99f37-113">參數</span><span class="sxs-lookup"><span data-stu-id="99f37-113">PARAMETERS</span></span>

### <span data-ttu-id="99f37-114">-ActiveDirectories</span><span class="sxs-lookup"><span data-stu-id="99f37-114">-ActiveDirectories</span></span>
<span data-ttu-id="99f37-115">代表活動目錄的 hashtable 陣列</span><span class="sxs-lookup"><span data-stu-id="99f37-115">A hashtable array which represents the active directories</span></span>

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

### <span data-ttu-id="99f37-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99f37-116">-DefaultProfile</span></span>
<span data-ttu-id="99f37-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="99f37-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="99f37-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="99f37-118">-InputObject</span></span>
<span data-ttu-id="99f37-119">要更新的帳戶物件</span><span class="sxs-lookup"><span data-stu-id="99f37-119">The account object to update</span></span>

```yaml
Type: PSNetAppFilesAccount
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="99f37-120">-位置</span><span class="sxs-lookup"><span data-stu-id="99f37-120">-Location</span></span>
<span data-ttu-id="99f37-121">資源的位置</span><span class="sxs-lookup"><span data-stu-id="99f37-121">The location of the resource</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99f37-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="99f37-122">-Name</span></span>
<span data-ttu-id="99f37-123">ANF 帳戶的名稱</span><span class="sxs-lookup"><span data-stu-id="99f37-123">The name of the ANF account</span></span>

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

### <span data-ttu-id="99f37-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="99f37-124">-ResourceGroupName</span></span>
<span data-ttu-id="99f37-125">ANF 帳戶的 [資源] 群組</span><span class="sxs-lookup"><span data-stu-id="99f37-125">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="99f37-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="99f37-126">-ResourceId</span></span>
<span data-ttu-id="99f37-127">ANF 帳戶的資源識別碼</span><span class="sxs-lookup"><span data-stu-id="99f37-127">The resource id of the ANF account</span></span>

```yaml
Type: String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="99f37-128">-Tag</span><span class="sxs-lookup"><span data-stu-id="99f37-128">-Tag</span></span>
<span data-ttu-id="99f37-129">代表資源標記的 hashtable</span><span class="sxs-lookup"><span data-stu-id="99f37-129">A hashtable which represents resource tags</span></span>

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

### <span data-ttu-id="99f37-130">-確認</span><span class="sxs-lookup"><span data-stu-id="99f37-130">-Confirm</span></span>
<span data-ttu-id="99f37-131">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="99f37-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="99f37-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="99f37-132">-WhatIf</span></span>
<span data-ttu-id="99f37-133">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="99f37-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="99f37-134">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="99f37-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="99f37-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99f37-135">CommonParameters</span></span>
<span data-ttu-id="99f37-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="99f37-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="99f37-137">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="99f37-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99f37-138">輸入</span><span class="sxs-lookup"><span data-stu-id="99f37-138">INPUTS</span></span>

### <span data-ttu-id="99f37-139">所有</span><span class="sxs-lookup"><span data-stu-id="99f37-139">None</span></span>

## <span data-ttu-id="99f37-140">輸出</span><span class="sxs-lookup"><span data-stu-id="99f37-140">OUTPUTS</span></span>

### <span data-ttu-id="99f37-141">PSNetAppFilesAccount 中的 NetAppFiles。</span><span class="sxs-lookup"><span data-stu-id="99f37-141">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="99f37-142">筆記</span><span class="sxs-lookup"><span data-stu-id="99f37-142">NOTES</span></span>

## <span data-ttu-id="99f37-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="99f37-143">RELATED LINKS</span></span>
