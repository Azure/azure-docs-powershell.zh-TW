---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: FFB335D4-AE3E-4788-B6FD-9AFC36F52B61
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreItemAcl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreItemAcl.md
ms.openlocfilehash: 94f81e8256af9282cdd5e09c1ab2822bf99c772f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93626009"
---
# <span data-ttu-id="358bc-101">Set-AzureRmDataLakeStoreItemAcl</span><span class="sxs-lookup"><span data-stu-id="358bc-101">Set-AzureRmDataLakeStoreItemAcl</span></span>

## <span data-ttu-id="358bc-102">摘要</span><span class="sxs-lookup"><span data-stu-id="358bc-102">SYNOPSIS</span></span>
<span data-ttu-id="358bc-103">修改 Data Lake Store 中檔案或資料夾的 ACL。</span><span class="sxs-lookup"><span data-stu-id="358bc-103">Modifies the ACL of a file or folder in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="358bc-104">句法</span><span class="sxs-lookup"><span data-stu-id="358bc-104">SYNTAX</span></span>

```
Set-AzureRmDataLakeStoreItemAcl [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-Acl] <DataLakeStoreItemAce[]> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="358bc-105">說明</span><span class="sxs-lookup"><span data-stu-id="358bc-105">DESCRIPTION</span></span>
<span data-ttu-id="358bc-106">**AzureRmDataLakeStoreItemAcl** Cmdlet 會修改 Data Lake store 中檔案或資料夾 (ACL) 的存取控制清單。</span><span class="sxs-lookup"><span data-stu-id="358bc-106">The **Set-AzureRmDataLakeStoreItemAcl** cmdlet modifies the access control list (ACL) of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="358bc-107">示例</span><span class="sxs-lookup"><span data-stu-id="358bc-107">EXAMPLES</span></span>

### <span data-ttu-id="358bc-108">範例1：設定檔案和資料夾的 ACL</span><span class="sxs-lookup"><span data-stu-id="358bc-108">Example 1: Set the ACL for a file and a folder</span></span>
```
PS C:\>$ACL = Get-AzureRmDataLakeStoreItemAcl -AccountName "ContosoADL" -Path /
PS C:\> Set-AzureRmDataLakeStoreItemAcl -AccountName "ContosoADL" -Path "/MyFiles/Test.txt" -Acl $ACL
```

<span data-ttu-id="358bc-109">第一個命令會取得 ContosoADL 帳戶之根目錄的 ACL，然後將其儲存在 $ACL 變數中。</span><span class="sxs-lookup"><span data-stu-id="358bc-109">The first command gets the ACL for the root directory of the ContosoADL account, and then stores it in the $ACL variable.</span></span>

<span data-ttu-id="358bc-110">第二個命令會將檔案 Test.txt 的 ACL 設定為 $ACL 中的那個檔案。</span><span class="sxs-lookup"><span data-stu-id="358bc-110">The second command sets the ACL for the file Test.txt to the one in $ACL.</span></span>

## <span data-ttu-id="358bc-111">參數</span><span class="sxs-lookup"><span data-stu-id="358bc-111">PARAMETERS</span></span>

### <span data-ttu-id="358bc-112">-帳戶</span><span class="sxs-lookup"><span data-stu-id="358bc-112">-Account</span></span>
<span data-ttu-id="358bc-113">指定 Data Lake Store 帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="358bc-113">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="358bc-114">-Acl</span><span class="sxs-lookup"><span data-stu-id="358bc-114">-Acl</span></span>
<span data-ttu-id="358bc-115">指定檔案或資料夾的 ACL。</span><span class="sxs-lookup"><span data-stu-id="358bc-115">Specifies an ACL for a file or a folder.</span></span>

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

### <span data-ttu-id="358bc-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="358bc-116">-PassThru</span></span>
<span data-ttu-id="358bc-117">指出應該傳回產生的 ACL。</span><span class="sxs-lookup"><span data-stu-id="358bc-117">Indicates the resulting ACL should be returned.</span></span>

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

### <span data-ttu-id="358bc-118">-Path</span><span class="sxs-lookup"><span data-stu-id="358bc-118">-Path</span></span>
<span data-ttu-id="358bc-119">指定檔案或資料夾的 Data Lake Store 路徑，從根目錄開始 (/) 。</span><span class="sxs-lookup"><span data-stu-id="358bc-119">Specifies the Data Lake Store path of the file or folder, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="358bc-120">-確認</span><span class="sxs-lookup"><span data-stu-id="358bc-120">-Confirm</span></span>
<span data-ttu-id="358bc-121">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="358bc-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="358bc-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="358bc-122">-WhatIf</span></span>
<span data-ttu-id="358bc-123">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="358bc-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="358bc-124">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="358bc-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="358bc-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="358bc-125">-DefaultProfile</span></span>
<span data-ttu-id="358bc-126">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="358bc-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="358bc-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="358bc-127">CommonParameters</span></span>
<span data-ttu-id="358bc-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="358bc-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="358bc-129">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="358bc-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="358bc-130">輸入</span><span class="sxs-lookup"><span data-stu-id="358bc-130">INPUTS</span></span>

### <span data-ttu-id="358bc-131">DataLakeStoreItemAce[]</span><span class="sxs-lookup"><span data-stu-id="358bc-131">DataLakeStoreItemAce[]</span></span>
<span data-ttu-id="358bc-132">[Acl "是從管線接受類型 ' DataLakeStoreItemAce []」的值</span><span class="sxs-lookup"><span data-stu-id="358bc-132">Parameter 'Acl' accepts value of type 'DataLakeStoreItemAce[]' from the pipeline</span></span>

## <span data-ttu-id="358bc-133">輸出</span><span class="sxs-lookup"><span data-stu-id="358bc-133">OUTPUTS</span></span>

### <span data-ttu-id="358bc-134">IEnumerable<DataLakeStoreItemAce></span><span class="sxs-lookup"><span data-stu-id="358bc-134">IEnumerable<DataLakeStoreItemAce></span></span>
<span data-ttu-id="358bc-135">如果已指定 PassThru，將會傳回產生的 ACL 專案清單。</span><span class="sxs-lookup"><span data-stu-id="358bc-135">If PassThru is specified, will return the resulting list of ACL entries.</span></span>

## <span data-ttu-id="358bc-136">筆記</span><span class="sxs-lookup"><span data-stu-id="358bc-136">NOTES</span></span>

## <span data-ttu-id="358bc-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="358bc-137">RELATED LINKS</span></span>

