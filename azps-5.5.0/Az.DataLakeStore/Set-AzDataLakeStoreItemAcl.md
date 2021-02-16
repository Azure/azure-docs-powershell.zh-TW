---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: FFB335D4-AE3E-4788-B6FD-9AFC36F52B61
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/set-azdatalakestoreitemacl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreItemAcl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreItemAcl.md
ms.openlocfilehash: 8b3412acd7513718c8c34e3fc8bb10c5e33f11a8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100133307"
---
# <span data-ttu-id="d5ada-101">Set-AzDataLakeStoreItemAcl</span><span class="sxs-lookup"><span data-stu-id="d5ada-101">Set-AzDataLakeStoreItemAcl</span></span>

## <span data-ttu-id="d5ada-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d5ada-102">SYNOPSIS</span></span>
<span data-ttu-id="d5ada-103">修改 Data Lake Store 中檔案或資料夾的 ACL。</span><span class="sxs-lookup"><span data-stu-id="d5ada-103">Modifies the ACL of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="d5ada-104">句法</span><span class="sxs-lookup"><span data-stu-id="d5ada-104">SYNTAX</span></span>

```
Set-AzDataLakeStoreItemAcl [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-Acl] <DataLakeStoreItemAce[]> [-PassThru] [-Recurse] [-Concurrency <Int32>] [-ShowProgress]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d5ada-105">說明</span><span class="sxs-lookup"><span data-stu-id="d5ada-105">DESCRIPTION</span></span>
<span data-ttu-id="d5ada-106">**AzDataLakeStoreItemAcl** Cmdlet 會修改 Data Lake store 中檔案或資料夾 (ACL) 的存取控制清單。</span><span class="sxs-lookup"><span data-stu-id="d5ada-106">The **Set-AzDataLakeStoreItemAcl** cmdlet modifies the access control list (ACL) of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="d5ada-107">示例</span><span class="sxs-lookup"><span data-stu-id="d5ada-107">EXAMPLES</span></span>

### <span data-ttu-id="d5ada-108">範例1：設定檔案和資料夾的 ACL</span><span class="sxs-lookup"><span data-stu-id="d5ada-108">Example 1: Set the ACL for a file and a folder</span></span>
```
PS C:\>$ACL = Get-AzDataLakeStoreItemAclEntry -AccountName "ContosoADL" -Path /
PS C:\> Set-AzDataLakeStoreItemAcl -AccountName "ContosoADL" -Path "/MyFiles/Test.txt" -Acl $ACL
```

<span data-ttu-id="d5ada-109">第一個命令會取得 ContosoADL 帳戶之根目錄的 ACL，然後將其儲存在 $ACL 變數中。</span><span class="sxs-lookup"><span data-stu-id="d5ada-109">The first command gets the ACL for the root directory of the ContosoADL account, and then stores it in the $ACL variable.</span></span>
<span data-ttu-id="d5ada-110">第二個命令會將檔案 Test.txt 的 ACL 設定為 $ACL 中的那個檔案。</span><span class="sxs-lookup"><span data-stu-id="d5ada-110">The second command sets the ACL for the file Test.txt to the one in $ACL.</span></span>

### <span data-ttu-id="d5ada-111">範例2：以遞迴方式設定資料夾的 ACL</span><span class="sxs-lookup"><span data-stu-id="d5ada-111">Example 2: Set the ACL for folder recursively</span></span>
```
PS C:\>$ACL = Get-AzDataLakeStoreItemAclEntry -AccountName "ContosoADL" -Path /Folder1
PS C:\> Set-AzDataLakeStoreItemAcl -AccountName "ContosoADL" -Path "/Folder2" -Acl $ACL -Recurse -Concurrency 128
```

<span data-ttu-id="d5ada-112">第一個命令會取得 ContosoADL 帳戶之目錄 Folder1 的 ACL，然後將其儲存在 $ACL 變數中。</span><span class="sxs-lookup"><span data-stu-id="d5ada-112">The first command gets the ACL for the directory Folder1 of the ContosoADL account, and then stores it in the $ACL variable.</span></span>
<span data-ttu-id="d5ada-113">第二個命令會以遞迴方式將 ACL 設定為 Folder2，並將它的子目錄和檔案設定為 $ACL。</span><span class="sxs-lookup"><span data-stu-id="d5ada-113">The second command sets the ACL recursively to Folder2 and its sub directories and files to the one in $ACL.</span></span>

## <span data-ttu-id="d5ada-114">參數</span><span class="sxs-lookup"><span data-stu-id="d5ada-114">PARAMETERS</span></span>

### <span data-ttu-id="d5ada-115">-帳戶</span><span class="sxs-lookup"><span data-stu-id="d5ada-115">-Account</span></span>
<span data-ttu-id="d5ada-116">指定 Data Lake Store 帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="d5ada-116">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="d5ada-117">-Acl</span><span class="sxs-lookup"><span data-stu-id="d5ada-117">-Acl</span></span>
<span data-ttu-id="d5ada-118">指定檔案或資料夾的 ACL。</span><span class="sxs-lookup"><span data-stu-id="d5ada-118">Specifies an ACL for a file or a folder.</span></span>

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

### <span data-ttu-id="d5ada-119">-併發性</span><span class="sxs-lookup"><span data-stu-id="d5ada-119">-Concurrency</span></span>
<span data-ttu-id="d5ada-120">並行處理的檔案/目錄數目。</span><span class="sxs-lookup"><span data-stu-id="d5ada-120">Number of files/directories processed in parallel.</span></span> <span data-ttu-id="d5ada-121">[選用]：將會選取合理的預設值。</span><span class="sxs-lookup"><span data-stu-id="d5ada-121">Optional: a reasonable default will be selected.</span></span>

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

### <span data-ttu-id="d5ada-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5ada-122">-DefaultProfile</span></span>
<span data-ttu-id="d5ada-123">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="d5ada-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d5ada-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d5ada-124">-PassThru</span></span>
<span data-ttu-id="d5ada-125">指出應該傳回產生的 ACL。</span><span class="sxs-lookup"><span data-stu-id="d5ada-125">Indicates the resulting ACL should be returned.</span></span>

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

### <span data-ttu-id="d5ada-126">-Path</span><span class="sxs-lookup"><span data-stu-id="d5ada-126">-Path</span></span>
<span data-ttu-id="d5ada-127">指定檔案或資料夾的 Data Lake Store 路徑，從根目錄開始 (/) 。</span><span class="sxs-lookup"><span data-stu-id="d5ada-127">Specifies the Data Lake Store path of the file or folder, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="d5ada-128">-遞迴</span><span class="sxs-lookup"><span data-stu-id="d5ada-128">-Recurse</span></span>
<span data-ttu-id="d5ada-129">指示要遞迴設定為子子目錄和檔案的 ACL</span><span class="sxs-lookup"><span data-stu-id="d5ada-129">Indicates the ACL to be set recursively to the child subdirectories and files</span></span>

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

### <span data-ttu-id="d5ada-130">-ShowProgress</span><span class="sxs-lookup"><span data-stu-id="d5ada-130">-ShowProgress</span></span>
<span data-ttu-id="d5ada-131">如果經過，就會顯示 [進度] 狀態。</span><span class="sxs-lookup"><span data-stu-id="d5ada-131">If passed then progress status is showed.</span></span> <span data-ttu-id="d5ada-132">只有在已完成遞迴 Acl 集時才適用。</span><span class="sxs-lookup"><span data-stu-id="d5ada-132">Only applicable when recursive Acl set is done.</span></span>

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

### <span data-ttu-id="d5ada-133">-確認</span><span class="sxs-lookup"><span data-stu-id="d5ada-133">-Confirm</span></span>
<span data-ttu-id="d5ada-134">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="d5ada-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d5ada-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d5ada-135">-WhatIf</span></span>
<span data-ttu-id="d5ada-136">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="d5ada-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d5ada-137">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d5ada-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d5ada-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5ada-138">CommonParameters</span></span>
<span data-ttu-id="d5ada-139">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d5ada-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5ada-140">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="d5ada-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5ada-141">輸入</span><span class="sxs-lookup"><span data-stu-id="d5ada-141">INPUTS</span></span>

### <span data-ttu-id="d5ada-142">System.object</span><span class="sxs-lookup"><span data-stu-id="d5ada-142">System.String</span></span>

### <span data-ttu-id="d5ada-143">DataLakeStorePathInstance 中的 DataLakeStore。</span><span class="sxs-lookup"><span data-stu-id="d5ada-143">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="d5ada-144">DataLakeStoreItemAce [] 的 DataLakeStore []</span><span class="sxs-lookup"><span data-stu-id="d5ada-144">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItemAce[]</span></span>

### <span data-ttu-id="d5ada-145">SwitchParameter 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="d5ada-145">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="d5ada-146">System.object</span><span class="sxs-lookup"><span data-stu-id="d5ada-146">System.Int32</span></span>

## <span data-ttu-id="d5ada-147">輸出</span><span class="sxs-lookup"><span data-stu-id="d5ada-147">OUTPUTS</span></span>

### <span data-ttu-id="d5ada-148">DataLakeStoreItemAce 中的 DataLakeStore。</span><span class="sxs-lookup"><span data-stu-id="d5ada-148">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItemAce</span></span>

## <span data-ttu-id="d5ada-149">筆記</span><span class="sxs-lookup"><span data-stu-id="d5ada-149">NOTES</span></span>

## <span data-ttu-id="d5ada-150">相關連結</span><span class="sxs-lookup"><span data-stu-id="d5ada-150">RELATED LINKS</span></span>
