---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: FFB335D4-AE3E-4788-B6FD-9AFC36F52B61
online version: https://docs.microsoft.com/powershell/module/az.datalakestore/set-azdatalakestoreitemacl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreItemAcl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreItemAcl.md
ms.openlocfilehash: 16663994a245a7429560ccf2ab855a84acc6ae57
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101902969"
---
# <span data-ttu-id="9d510-101">Set-AzDataLakeStoreItemAcl</span><span class="sxs-lookup"><span data-stu-id="9d510-101">Set-AzDataLakeStoreItemAcl</span></span>

## <span data-ttu-id="9d510-102">簡介</span><span class="sxs-lookup"><span data-stu-id="9d510-102">SYNOPSIS</span></span>
<span data-ttu-id="9d510-103">修改 Data Lake Store 中檔案或資料夾的 ACL。</span><span class="sxs-lookup"><span data-stu-id="9d510-103">Modifies the ACL of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="9d510-104">語法</span><span class="sxs-lookup"><span data-stu-id="9d510-104">SYNTAX</span></span>

```
Set-AzDataLakeStoreItemAcl [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-Acl] <DataLakeStoreItemAce[]> [-PassThru] [-Recurse] [-Concurrency <Int32>] [-ShowProgress]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9d510-105">描述</span><span class="sxs-lookup"><span data-stu-id="9d510-105">DESCRIPTION</span></span>
<span data-ttu-id="9d510-106">**Set-AzDataLakeStoreItemAcl** Cmdlet 會修改 Data Lake Store 中檔案或資料夾的存取控制清單 (ACL) 。</span><span class="sxs-lookup"><span data-stu-id="9d510-106">The **Set-AzDataLakeStoreItemAcl** cmdlet modifies the access control list (ACL) of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="9d510-107">例子</span><span class="sxs-lookup"><span data-stu-id="9d510-107">EXAMPLES</span></span>

### <span data-ttu-id="9d510-108">範例 1：設定檔案和資料夾的 ACL</span><span class="sxs-lookup"><span data-stu-id="9d510-108">Example 1: Set the ACL for a file and a folder</span></span>
```
PS C:\>$ACL = Get-AzDataLakeStoreItemAclEntry -AccountName "ContosoADL" -Path /
PS C:\> Set-AzDataLakeStoreItemAcl -AccountName "ContosoADL" -Path "/MyFiles/Test.txt" -Acl $ACL
```

<span data-ttu-id="9d510-109">第一個命令會獲得 ContosoADL 帳戶根目錄的 ACL，然後將它儲存在$ACL變數。</span><span class="sxs-lookup"><span data-stu-id="9d510-109">The first command gets the ACL for the root directory of the ContosoADL account, and then stores it in the $ACL variable.</span></span>
<span data-ttu-id="9d510-110">第二個命令會設定檔案的 ACL，Test.txt中該檔案的$ACL。</span><span class="sxs-lookup"><span data-stu-id="9d510-110">The second command sets the ACL for the file Test.txt to the one in $ACL.</span></span>

### <span data-ttu-id="9d510-111">範例 2：設定資料夾遞迴的 ACL</span><span class="sxs-lookup"><span data-stu-id="9d510-111">Example 2: Set the ACL for folder recursively</span></span>
```
PS C:\>$ACL = Get-AzDataLakeStoreItemAclEntry -AccountName "ContosoADL" -Path /Folder1
PS C:\> Set-AzDataLakeStoreItemAcl -AccountName "ContosoADL" -Path "/Folder2" -Acl $ACL -Recurse -Concurrency 128
```

<span data-ttu-id="9d510-112">第一個命令會獲得 ContosoADL 帳戶目錄資料夾1 的 ACL，然後將它儲存在$ACL變數。</span><span class="sxs-lookup"><span data-stu-id="9d510-112">The first command gets the ACL for the directory Folder1 of the ContosoADL account, and then stores it in the $ACL variable.</span></span>
<span data-ttu-id="9d510-113">第二個命令會以遞迴方式將 ACL 設定為 Folder2 及其子目錄和檔案，$ACL。</span><span class="sxs-lookup"><span data-stu-id="9d510-113">The second command sets the ACL recursively to Folder2 and its sub directories and files to the one in $ACL.</span></span>

## <span data-ttu-id="9d510-114">參數</span><span class="sxs-lookup"><span data-stu-id="9d510-114">PARAMETERS</span></span>

### <span data-ttu-id="9d510-115">-帳戶</span><span class="sxs-lookup"><span data-stu-id="9d510-115">-Account</span></span>
<span data-ttu-id="9d510-116">指定 Data Lake Store 帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="9d510-116">Specifies the name of the Data Lake Store account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9d510-117">-Acl</span><span class="sxs-lookup"><span data-stu-id="9d510-117">-Acl</span></span>
<span data-ttu-id="9d510-118">指定檔案或資料夾的 ACL。</span><span class="sxs-lookup"><span data-stu-id="9d510-118">Specifies an ACL for a file or a folder.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItemAce[]
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9d510-119">-並行</span><span class="sxs-lookup"><span data-stu-id="9d510-119">-Concurrency</span></span>
<span data-ttu-id="9d510-120">平行處理的檔案/目錄數目。</span><span class="sxs-lookup"><span data-stu-id="9d510-120">Number of files/directories processed in parallel.</span></span> <span data-ttu-id="9d510-121">選擇性：會選取合理的預設值。</span><span class="sxs-lookup"><span data-stu-id="9d510-121">Optional: a reasonable default will be selected.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9d510-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9d510-122">-DefaultProfile</span></span>
<span data-ttu-id="9d510-123">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="9d510-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9d510-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9d510-124">-PassThru</span></span>
<span data-ttu-id="9d510-125">表示應該會退回產生的 ACL。</span><span class="sxs-lookup"><span data-stu-id="9d510-125">Indicates the resulting ACL should be returned.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9d510-126">-路徑</span><span class="sxs-lookup"><span data-stu-id="9d510-126">-Path</span></span>
<span data-ttu-id="9d510-127">指定檔案或資料夾的 Data Lake Store 路徑，從根目錄開始 (/) 。</span><span class="sxs-lookup"><span data-stu-id="9d510-127">Specifies the Data Lake Store path of the file or folder, starting with the root directory (/).</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9d510-128">-遞迴</span><span class="sxs-lookup"><span data-stu-id="9d510-128">-Recurse</span></span>
<span data-ttu-id="9d510-129">表示要以遞迴性設定為子子目錄和檔案的 ACL</span><span class="sxs-lookup"><span data-stu-id="9d510-129">Indicates the ACL to be set recursively to the child subdirectories and files</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9d510-130">-ShowProgress</span><span class="sxs-lookup"><span data-stu-id="9d510-130">-ShowProgress</span></span>
<span data-ttu-id="9d510-131">如果通過，則顯示進度狀態。</span><span class="sxs-lookup"><span data-stu-id="9d510-131">If passed then progress status is showed.</span></span> <span data-ttu-id="9d510-132">只有在完成遞迴 Acl 集時適用。</span><span class="sxs-lookup"><span data-stu-id="9d510-132">Only applicable when recursive Acl set is done.</span></span>

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

### <span data-ttu-id="9d510-133">-確認</span><span class="sxs-lookup"><span data-stu-id="9d510-133">-Confirm</span></span>
<span data-ttu-id="9d510-134">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="9d510-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9d510-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9d510-135">-WhatIf</span></span>
<span data-ttu-id="9d510-136">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="9d510-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9d510-137">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="9d510-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9d510-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d510-138">CommonParameters</span></span>
<span data-ttu-id="9d510-139">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="9d510-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d510-140">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="9d510-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d510-141">輸入</span><span class="sxs-lookup"><span data-stu-id="9d510-141">INPUTS</span></span>

### <span data-ttu-id="9d510-142">System.String</span><span class="sxs-lookup"><span data-stu-id="9d510-142">System.String</span></span>

### <span data-ttu-id="9d510-143">Microsoft.Azure.Commands.DataLakeStore.models.DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="9d510-143">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="9d510-144">Microsoft.Azure.Commands.DataLakeStore.models.DataLakeStoreItemAce[]</span><span class="sxs-lookup"><span data-stu-id="9d510-144">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItemAce[]</span></span>

### <span data-ttu-id="9d510-145">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="9d510-145">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="9d510-146">System.Int32</span><span class="sxs-lookup"><span data-stu-id="9d510-146">System.Int32</span></span>

## <span data-ttu-id="9d510-147">輸出</span><span class="sxs-lookup"><span data-stu-id="9d510-147">OUTPUTS</span></span>

### <span data-ttu-id="9d510-148">Microsoft.Azure.Commands.DataLakeStore.models.DataLakeStoreItemAce</span><span class="sxs-lookup"><span data-stu-id="9d510-148">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItemAce</span></span>

## <span data-ttu-id="9d510-149">筆記</span><span class="sxs-lookup"><span data-stu-id="9d510-149">NOTES</span></span>

## <span data-ttu-id="9d510-150">相關連結</span><span class="sxs-lookup"><span data-stu-id="9d510-150">RELATED LINKS</span></span>
