---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: FFB335D4-AE3E-4788-B6FD-9AFC36F52B61
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/set-azdatalakestoreitemacl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreItemAcl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreItemAcl.md
ms.openlocfilehash: 8b3412acd7513718c8c34e3fc8bb10c5e33f11a8
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94126543"
---
# <span data-ttu-id="bd138-101">Set-AzDataLakeStoreItemAcl</span><span class="sxs-lookup"><span data-stu-id="bd138-101">Set-AzDataLakeStoreItemAcl</span></span>

## <span data-ttu-id="bd138-102">摘要</span><span class="sxs-lookup"><span data-stu-id="bd138-102">SYNOPSIS</span></span>
<span data-ttu-id="bd138-103">修改 Data Lake Store 中檔案或資料夾的 ACL。</span><span class="sxs-lookup"><span data-stu-id="bd138-103">Modifies the ACL of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="bd138-104">句法</span><span class="sxs-lookup"><span data-stu-id="bd138-104">SYNTAX</span></span>

```
Set-AzDataLakeStoreItemAcl [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-Acl] <DataLakeStoreItemAce[]> [-PassThru] [-Recurse] [-Concurrency <Int32>] [-ShowProgress]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bd138-105">說明</span><span class="sxs-lookup"><span data-stu-id="bd138-105">DESCRIPTION</span></span>
<span data-ttu-id="bd138-106">**AzDataLakeStoreItemAcl** Cmdlet 會修改 Data Lake store 中檔案或資料夾 (ACL) 的存取控制清單。</span><span class="sxs-lookup"><span data-stu-id="bd138-106">The **Set-AzDataLakeStoreItemAcl** cmdlet modifies the access control list (ACL) of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="bd138-107">示例</span><span class="sxs-lookup"><span data-stu-id="bd138-107">EXAMPLES</span></span>

### <span data-ttu-id="bd138-108">範例1：設定檔案和資料夾的 ACL</span><span class="sxs-lookup"><span data-stu-id="bd138-108">Example 1: Set the ACL for a file and a folder</span></span>
```
PS C:\>$ACL = Get-AzDataLakeStoreItemAclEntry -AccountName "ContosoADL" -Path /
PS C:\> Set-AzDataLakeStoreItemAcl -AccountName "ContosoADL" -Path "/MyFiles/Test.txt" -Acl $ACL
```

<span data-ttu-id="bd138-109">第一個命令會取得 ContosoADL 帳戶之根目錄的 ACL，然後將其儲存在 $ACL 變數中。</span><span class="sxs-lookup"><span data-stu-id="bd138-109">The first command gets the ACL for the root directory of the ContosoADL account, and then stores it in the $ACL variable.</span></span>
<span data-ttu-id="bd138-110">第二個命令會將檔案 Test.txt 的 ACL 設定為 $ACL 中的那個檔案。</span><span class="sxs-lookup"><span data-stu-id="bd138-110">The second command sets the ACL for the file Test.txt to the one in $ACL.</span></span>

### <span data-ttu-id="bd138-111">範例2：以遞迴方式設定資料夾的 ACL</span><span class="sxs-lookup"><span data-stu-id="bd138-111">Example 2: Set the ACL for folder recursively</span></span>
```
PS C:\>$ACL = Get-AzDataLakeStoreItemAclEntry -AccountName "ContosoADL" -Path /Folder1
PS C:\> Set-AzDataLakeStoreItemAcl -AccountName "ContosoADL" -Path "/Folder2" -Acl $ACL -Recurse -Concurrency 128
```

<span data-ttu-id="bd138-112">第一個命令會取得 ContosoADL 帳戶之目錄 Folder1 的 ACL，然後將其儲存在 $ACL 變數中。</span><span class="sxs-lookup"><span data-stu-id="bd138-112">The first command gets the ACL for the directory Folder1 of the ContosoADL account, and then stores it in the $ACL variable.</span></span>
<span data-ttu-id="bd138-113">第二個命令會以遞迴方式將 ACL 設定為 Folder2，並將它的子目錄和檔案設定為 $ACL。</span><span class="sxs-lookup"><span data-stu-id="bd138-113">The second command sets the ACL recursively to Folder2 and its sub directories and files to the one in $ACL.</span></span>

## <span data-ttu-id="bd138-114">參數</span><span class="sxs-lookup"><span data-stu-id="bd138-114">PARAMETERS</span></span>

### <span data-ttu-id="bd138-115">-帳戶</span><span class="sxs-lookup"><span data-stu-id="bd138-115">-Account</span></span>
<span data-ttu-id="bd138-116">指定 Data Lake Store 帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="bd138-116">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="bd138-117">-Acl</span><span class="sxs-lookup"><span data-stu-id="bd138-117">-Acl</span></span>
<span data-ttu-id="bd138-118">指定檔案或資料夾的 ACL。</span><span class="sxs-lookup"><span data-stu-id="bd138-118">Specifies an ACL for a file or a folder.</span></span>

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

### <span data-ttu-id="bd138-119">-併發性</span><span class="sxs-lookup"><span data-stu-id="bd138-119">-Concurrency</span></span>
<span data-ttu-id="bd138-120">並行處理的檔案/目錄數目。</span><span class="sxs-lookup"><span data-stu-id="bd138-120">Number of files/directories processed in parallel.</span></span> <span data-ttu-id="bd138-121">[選用]：將會選取合理的預設值。</span><span class="sxs-lookup"><span data-stu-id="bd138-121">Optional: a reasonable default will be selected.</span></span>

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

### <span data-ttu-id="bd138-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd138-122">-DefaultProfile</span></span>
<span data-ttu-id="bd138-123">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="bd138-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bd138-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bd138-124">-PassThru</span></span>
<span data-ttu-id="bd138-125">指出應該傳回產生的 ACL。</span><span class="sxs-lookup"><span data-stu-id="bd138-125">Indicates the resulting ACL should be returned.</span></span>

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

### <span data-ttu-id="bd138-126">-Path</span><span class="sxs-lookup"><span data-stu-id="bd138-126">-Path</span></span>
<span data-ttu-id="bd138-127">指定檔案或資料夾的 Data Lake Store 路徑，從根目錄開始 (/) 。</span><span class="sxs-lookup"><span data-stu-id="bd138-127">Specifies the Data Lake Store path of the file or folder, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="bd138-128">-遞迴</span><span class="sxs-lookup"><span data-stu-id="bd138-128">-Recurse</span></span>
<span data-ttu-id="bd138-129">指示要遞迴設定為子子目錄和檔案的 ACL</span><span class="sxs-lookup"><span data-stu-id="bd138-129">Indicates the ACL to be set recursively to the child subdirectories and files</span></span>

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

### <span data-ttu-id="bd138-130">-ShowProgress</span><span class="sxs-lookup"><span data-stu-id="bd138-130">-ShowProgress</span></span>
<span data-ttu-id="bd138-131">如果經過，就會顯示 [進度] 狀態。</span><span class="sxs-lookup"><span data-stu-id="bd138-131">If passed then progress status is showed.</span></span> <span data-ttu-id="bd138-132">只有在已完成遞迴 Acl 集時才適用。</span><span class="sxs-lookup"><span data-stu-id="bd138-132">Only applicable when recursive Acl set is done.</span></span>

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

### <span data-ttu-id="bd138-133">-確認</span><span class="sxs-lookup"><span data-stu-id="bd138-133">-Confirm</span></span>
<span data-ttu-id="bd138-134">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="bd138-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bd138-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bd138-135">-WhatIf</span></span>
<span data-ttu-id="bd138-136">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="bd138-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bd138-137">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="bd138-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bd138-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd138-138">CommonParameters</span></span>
<span data-ttu-id="bd138-139">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="bd138-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd138-140">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="bd138-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd138-141">輸入</span><span class="sxs-lookup"><span data-stu-id="bd138-141">INPUTS</span></span>

### <span data-ttu-id="bd138-142">System.object</span><span class="sxs-lookup"><span data-stu-id="bd138-142">System.String</span></span>

### <span data-ttu-id="bd138-143">DataLakeStorePathInstance 中的 DataLakeStore。</span><span class="sxs-lookup"><span data-stu-id="bd138-143">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="bd138-144">DataLakeStoreItemAce [] 的 DataLakeStore []</span><span class="sxs-lookup"><span data-stu-id="bd138-144">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItemAce[]</span></span>

### <span data-ttu-id="bd138-145">SwitchParameter 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="bd138-145">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="bd138-146">System.object</span><span class="sxs-lookup"><span data-stu-id="bd138-146">System.Int32</span></span>

## <span data-ttu-id="bd138-147">輸出</span><span class="sxs-lookup"><span data-stu-id="bd138-147">OUTPUTS</span></span>

### <span data-ttu-id="bd138-148">DataLakeStoreItemAce 中的 DataLakeStore。</span><span class="sxs-lookup"><span data-stu-id="bd138-148">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItemAce</span></span>

## <span data-ttu-id="bd138-149">筆記</span><span class="sxs-lookup"><span data-stu-id="bd138-149">NOTES</span></span>

## <span data-ttu-id="bd138-150">相關連結</span><span class="sxs-lookup"><span data-stu-id="bd138-150">RELATED LINKS</span></span>
