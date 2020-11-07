---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 6ACE045E-67AD-40FE-86E4-450AF522F174
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/set-azdatalakestoreitempermission
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreItemPermission.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreItemPermission.md
ms.openlocfilehash: af14588394a94e771c1287081aa263a7ba8e9da1
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93966467"
---
# <span data-ttu-id="c7309-101">Set-AzDataLakeStoreItemPermission</span><span class="sxs-lookup"><span data-stu-id="c7309-101">Set-AzDataLakeStoreItemPermission</span></span>

## <span data-ttu-id="c7309-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c7309-102">SYNOPSIS</span></span>
<span data-ttu-id="c7309-103">修改 Data Lake Store 中檔案或資料夾的許可權八進位。</span><span class="sxs-lookup"><span data-stu-id="c7309-103">Modifies the permission octal of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="c7309-104">句法</span><span class="sxs-lookup"><span data-stu-id="c7309-104">SYNTAX</span></span>

```
Set-AzDataLakeStoreItemPermission [-Account] <String> [-Path] <DataLakeStorePathInstance> [-Permission] <Int32>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c7309-105">說明</span><span class="sxs-lookup"><span data-stu-id="c7309-105">DESCRIPTION</span></span>
<span data-ttu-id="c7309-106">**AzDataLakeStoreItemPermission** Cmdlet 會修改 Data Lake store 中檔案或資料夾的許可權八進位。</span><span class="sxs-lookup"><span data-stu-id="c7309-106">The **Set-AzDataLakeStoreItemPermission** cmdlet modifies the permission octal of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="c7309-107">示例</span><span class="sxs-lookup"><span data-stu-id="c7309-107">EXAMPLES</span></span>

### <span data-ttu-id="c7309-108">範例1：設定專案的許可權八進位</span><span class="sxs-lookup"><span data-stu-id="c7309-108">Example 1: Set the permission octal for an item</span></span>
```
PS C:\>Set-AzDataLakeStoreItemPermission -AccountName "ContosoADL" -Path "/file.txt" -Permission 0770
```

<span data-ttu-id="c7309-109">這個命令會將檔案的許可權八進位設定為0770，轉換成清除粘滯位、設定檔案擁有者的讀/寫/執行許可權、設定檔案擁有者群組的讀取/寫入/執行許可權，以及清除其他人的讀取/寫入/執行許可權。</span><span class="sxs-lookup"><span data-stu-id="c7309-109">This command sets the permission octal for a file to 0770, which translates to clearing the sticky bit, setting read/write/execute permissions for the owner of the file, setting read/write/execute permissions for the owning group of the file, and clearing read/write/execute permissions for other.</span></span>

## <span data-ttu-id="c7309-110">參數</span><span class="sxs-lookup"><span data-stu-id="c7309-110">PARAMETERS</span></span>

### <span data-ttu-id="c7309-111">-帳戶</span><span class="sxs-lookup"><span data-stu-id="c7309-111">-Account</span></span>
<span data-ttu-id="c7309-112">指定 Data Lake Store 帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="c7309-112">Specifies the Data Lake Store account name.</span></span>

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

### <span data-ttu-id="c7309-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7309-113">-DefaultProfile</span></span>
<span data-ttu-id="c7309-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="c7309-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c7309-115">-Path</span><span class="sxs-lookup"><span data-stu-id="c7309-115">-Path</span></span>
<span data-ttu-id="c7309-116">指定檔案或資料夾的 Data Lake Store 路徑，從根目錄開始 (/) 。</span><span class="sxs-lookup"><span data-stu-id="c7309-116">Specifies the Data Lake Store path of the file or folder, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="c7309-117">-許可權</span><span class="sxs-lookup"><span data-stu-id="c7309-117">-Permission</span></span>
<span data-ttu-id="c7309-118">要為檔案或資料夾設定的許可權，以八進位 (（例如 "777"） ) </span><span class="sxs-lookup"><span data-stu-id="c7309-118">The permissions to set for the file or folder, expressed as an octal (e.g. '777')</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c7309-119">-確認</span><span class="sxs-lookup"><span data-stu-id="c7309-119">-Confirm</span></span>
<span data-ttu-id="c7309-120">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="c7309-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c7309-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c7309-121">-WhatIf</span></span>
<span data-ttu-id="c7309-122">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="c7309-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c7309-123">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c7309-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c7309-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7309-124">CommonParameters</span></span>
<span data-ttu-id="c7309-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c7309-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7309-126">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="c7309-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7309-127">輸入</span><span class="sxs-lookup"><span data-stu-id="c7309-127">INPUTS</span></span>

### <span data-ttu-id="c7309-128">System.object</span><span class="sxs-lookup"><span data-stu-id="c7309-128">System.String</span></span>

### <span data-ttu-id="c7309-129">DataLakeStorePathInstance 中的 DataLakeStore。</span><span class="sxs-lookup"><span data-stu-id="c7309-129">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="c7309-130">System.object</span><span class="sxs-lookup"><span data-stu-id="c7309-130">System.Int32</span></span>

## <span data-ttu-id="c7309-131">輸出</span><span class="sxs-lookup"><span data-stu-id="c7309-131">OUTPUTS</span></span>

### <span data-ttu-id="c7309-132">System.object</span><span class="sxs-lookup"><span data-stu-id="c7309-132">System.Boolean</span></span>

## <span data-ttu-id="c7309-133">筆記</span><span class="sxs-lookup"><span data-stu-id="c7309-133">NOTES</span></span>
* <span data-ttu-id="c7309-134">別名： Set-AdlStoreItemPermission</span><span class="sxs-lookup"><span data-stu-id="c7309-134">Alias: Set-AdlStoreItemPermission</span></span>

## <span data-ttu-id="c7309-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="c7309-135">RELATED LINKS</span></span>

[<span data-ttu-id="c7309-136">AzDataLakeStoreItemPermission</span><span class="sxs-lookup"><span data-stu-id="c7309-136">Get-AzDataLakeStoreItemPermission</span></span>](./Get-AzDataLakeStoreItemPermission.md)


