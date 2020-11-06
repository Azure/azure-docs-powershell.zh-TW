---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 6ACE045E-67AD-40FE-86E4-450AF522F174
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/set-azurermdatalakestoreitempermission
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreItemPermission.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreItemPermission.md
ms.openlocfilehash: 82dac83b9e252e154cedb50f7a3b90a1a78c01c0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93451520"
---
# <span data-ttu-id="8b7bf-101">Set-AzureRmDataLakeStoreItemPermission</span><span class="sxs-lookup"><span data-stu-id="8b7bf-101">Set-AzureRmDataLakeStoreItemPermission</span></span>

## <span data-ttu-id="8b7bf-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8b7bf-102">SYNOPSIS</span></span>
<span data-ttu-id="8b7bf-103">修改 Data Lake Store 中檔案或資料夾的許可權八進位。</span><span class="sxs-lookup"><span data-stu-id="8b7bf-103">Modifies the permission octal of a file or folder in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8b7bf-104">句法</span><span class="sxs-lookup"><span data-stu-id="8b7bf-104">SYNTAX</span></span>

```
Set-AzureRmDataLakeStoreItemPermission [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-Permission] <Int32> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8b7bf-105">說明</span><span class="sxs-lookup"><span data-stu-id="8b7bf-105">DESCRIPTION</span></span>
<span data-ttu-id="8b7bf-106">**AzureRmDataLakeStoreItemPermission** Cmdlet 會修改 Data Lake store 中檔案或資料夾的許可權八進位。</span><span class="sxs-lookup"><span data-stu-id="8b7bf-106">The **Set-AzureRmDataLakeStoreItemPermission** cmdlet modifies the permission octal of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="8b7bf-107">示例</span><span class="sxs-lookup"><span data-stu-id="8b7bf-107">EXAMPLES</span></span>

### <span data-ttu-id="8b7bf-108">範例1：設定專案的許可權八進位</span><span class="sxs-lookup"><span data-stu-id="8b7bf-108">Example 1: Set the permission octal for an item</span></span>
```
PS C:\>Set-AzureRmDataLakeStoreItemPermission -AccountName "ContosoADL" -Path "/file.txt" -Permission 0770
```

<span data-ttu-id="8b7bf-109">這個命令會將檔案的許可權八進位設定為0770，轉換成清除粘滯位、設定檔案擁有者的讀/寫/執行許可權、設定檔案擁有者群組的讀取/寫入/執行許可權，以及清除其他人的讀取/寫入/執行許可權。</span><span class="sxs-lookup"><span data-stu-id="8b7bf-109">This command sets the permission octal for a file to 0770, which translates to clearing the sticky bit, setting read/write/execute permissions for the owner of the file, setting read/write/execute permissions for the owning group of the file, and clearing read/write/execute permissions for other.</span></span>

## <span data-ttu-id="8b7bf-110">參數</span><span class="sxs-lookup"><span data-stu-id="8b7bf-110">PARAMETERS</span></span>

### <span data-ttu-id="8b7bf-111">-帳戶</span><span class="sxs-lookup"><span data-stu-id="8b7bf-111">-Account</span></span>
<span data-ttu-id="8b7bf-112">指定 Data Lake Store 帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="8b7bf-112">Specifies the Data Lake Store account name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8b7bf-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b7bf-113">-DefaultProfile</span></span>
<span data-ttu-id="8b7bf-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="8b7bf-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b7bf-115">-Path</span><span class="sxs-lookup"><span data-stu-id="8b7bf-115">-Path</span></span>
<span data-ttu-id="8b7bf-116">指定檔案或資料夾的 Data Lake Store 路徑，從根目錄開始 (/) 。</span><span class="sxs-lookup"><span data-stu-id="8b7bf-116">Specifies the Data Lake Store path of the file or folder, starting with the root directory (/).</span></span>

```yaml
Type: DataLakeStorePathInstance
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8b7bf-117">-許可權</span><span class="sxs-lookup"><span data-stu-id="8b7bf-117">-Permission</span></span>
<span data-ttu-id="8b7bf-118">要為檔案或資料夾設定的許可權，以八進位 (（例如 "777"） ) </span><span class="sxs-lookup"><span data-stu-id="8b7bf-118">The permissions to set for the file or folder, expressed as an octal (e.g. '777')</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8b7bf-119">-確認</span><span class="sxs-lookup"><span data-stu-id="8b7bf-119">-Confirm</span></span>
<span data-ttu-id="8b7bf-120">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="8b7bf-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b7bf-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8b7bf-121">-WhatIf</span></span>
<span data-ttu-id="8b7bf-122">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="8b7bf-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8b7bf-123">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8b7bf-123">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b7bf-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b7bf-124">CommonParameters</span></span>
<span data-ttu-id="8b7bf-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8b7bf-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b7bf-126">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="8b7bf-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b7bf-127">輸入</span><span class="sxs-lookup"><span data-stu-id="8b7bf-127">INPUTS</span></span>

### <span data-ttu-id="8b7bf-128">所有</span><span class="sxs-lookup"><span data-stu-id="8b7bf-128">None</span></span>
<span data-ttu-id="8b7bf-129">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="8b7bf-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="8b7bf-130">輸出</span><span class="sxs-lookup"><span data-stu-id="8b7bf-130">OUTPUTS</span></span>

### <span data-ttu-id="8b7bf-131">bool</span><span class="sxs-lookup"><span data-stu-id="8b7bf-131">bool</span></span>
<span data-ttu-id="8b7bf-132">成功更新許可權時，傳回 true。</span><span class="sxs-lookup"><span data-stu-id="8b7bf-132">Returns true upon successfully updating the permission.</span></span>

## <span data-ttu-id="8b7bf-133">筆記</span><span class="sxs-lookup"><span data-stu-id="8b7bf-133">NOTES</span></span>
* <span data-ttu-id="8b7bf-134">別名： Set-AdlStoreItemPermission</span><span class="sxs-lookup"><span data-stu-id="8b7bf-134">Alias: Set-AdlStoreItemPermission</span></span>

## <span data-ttu-id="8b7bf-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="8b7bf-135">RELATED LINKS</span></span>

[<span data-ttu-id="8b7bf-136">AzureRmDataLakeStoreItemPermission</span><span class="sxs-lookup"><span data-stu-id="8b7bf-136">Get-AzureRmDataLakeStoreItemPermission</span></span>](./Get-AzureRmDataLakeStoreItemPermission.md)


