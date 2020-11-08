---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/disable-azstorageblobrestorepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Disable-AzStorageBlobRestorePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Disable-AzStorageBlobRestorePolicy.md
ms.openlocfilehash: 8e68400eeaedd6529ffc4069b36c6f73e25864f1
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "93971651"
---
# <span data-ttu-id="d2c1a-101">Disable-AzStorageBlobRestorePolicy</span><span class="sxs-lookup"><span data-stu-id="d2c1a-101">Disable-AzStorageBlobRestorePolicy</span></span>

## <span data-ttu-id="d2c1a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d2c1a-102">SYNOPSIS</span></span>
<span data-ttu-id="d2c1a-103">在儲存空間帳戶上停用 Blob 還原原則。</span><span class="sxs-lookup"><span data-stu-id="d2c1a-103">Disables Blob Restore Policy on a Storage account.</span></span>

## <span data-ttu-id="d2c1a-104">句法</span><span class="sxs-lookup"><span data-stu-id="d2c1a-104">SYNTAX</span></span>

### <span data-ttu-id="d2c1a-105">AccountName (預設) </span><span class="sxs-lookup"><span data-stu-id="d2c1a-105">AccountName (Default)</span></span>
```
Disable-AzStorageBlobRestorePolicy [-ResourceGroupName] <String> [-StorageAccountName] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d2c1a-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="d2c1a-106">AccountObject</span></span>
```
Disable-AzStorageBlobRestorePolicy -StorageAccount <PSStorageAccount> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d2c1a-107">BlobServicePropertiesResourceId</span><span class="sxs-lookup"><span data-stu-id="d2c1a-107">BlobServicePropertiesResourceId</span></span>
```
Disable-AzStorageBlobRestorePolicy [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d2c1a-108">說明</span><span class="sxs-lookup"><span data-stu-id="d2c1a-108">DESCRIPTION</span></span>
<span data-ttu-id="d2c1a-109">**Disable AzStorageBlobRestorePolicy** Cmdlet 會針對 Azure Storage Blob 服務停用 Blob 還原原則。</span><span class="sxs-lookup"><span data-stu-id="d2c1a-109">The **Disable-AzStorageBlobRestorePolicy** cmdlet disables Blob Restore Policy for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="d2c1a-110">示例</span><span class="sxs-lookup"><span data-stu-id="d2c1a-110">EXAMPLES</span></span>

### <span data-ttu-id="d2c1a-111">範例1：針對儲存帳戶上的 Azure Storage Blob 服務停用 Blob 還原原則</span><span class="sxs-lookup"><span data-stu-id="d2c1a-111">Example 1: Disables Blob Restore Policy for the Azure Storage Blob service on a Storage account</span></span>
```powershell
PS C:\> Disable-AzStorageBlobRestorePolicy -ResourceGroupName "myresourcegoup" -StorageAccountName "mystorageaccount"
```

<span data-ttu-id="d2c1a-112">這個命令會針對儲存帳戶上的 Azure Storage Blob 服務停用 Blob 還原原則。</span><span class="sxs-lookup"><span data-stu-id="d2c1a-112">This command Disables Blob Restore Policy for the Azure Storage Blob service on a Storage account.</span></span>

## <span data-ttu-id="d2c1a-113">參數</span><span class="sxs-lookup"><span data-stu-id="d2c1a-113">PARAMETERS</span></span>

### <span data-ttu-id="d2c1a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2c1a-114">-DefaultProfile</span></span>
<span data-ttu-id="d2c1a-115">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="d2c1a-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d2c1a-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d2c1a-116">-PassThru</span></span>
<span data-ttu-id="d2c1a-117">顯示 ServiceProperties</span><span class="sxs-lookup"><span data-stu-id="d2c1a-117">Display ServiceProperties</span></span>

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

### <span data-ttu-id="d2c1a-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d2c1a-118">-ResourceGroupName</span></span>
<span data-ttu-id="d2c1a-119">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="d2c1a-119">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2c1a-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d2c1a-120">-ResourceId</span></span>
<span data-ttu-id="d2c1a-121">輸入儲存空間帳戶資源識別碼，或 [Blob 服務屬性] 資源 Id。</span><span class="sxs-lookup"><span data-stu-id="d2c1a-121">Input a Storage account Resource Id, or a Blob service properties Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: BlobServicePropertiesResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d2c1a-122">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="d2c1a-122">-StorageAccount</span></span>
<span data-ttu-id="d2c1a-123">儲存空間帳戶物件</span><span class="sxs-lookup"><span data-stu-id="d2c1a-123">Storage account object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount
Parameter Sets: AccountObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d2c1a-124">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="d2c1a-124">-StorageAccountName</span></span>
<span data-ttu-id="d2c1a-125">儲存空間帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="d2c1a-125">Storage Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases: AccountName, Name

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2c1a-126">-確認</span><span class="sxs-lookup"><span data-stu-id="d2c1a-126">-Confirm</span></span>
<span data-ttu-id="d2c1a-127">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="d2c1a-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d2c1a-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d2c1a-128">-WhatIf</span></span>
<span data-ttu-id="d2c1a-129">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="d2c1a-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d2c1a-130">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d2c1a-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d2c1a-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2c1a-131">CommonParameters</span></span>
<span data-ttu-id="d2c1a-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d2c1a-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2c1a-133">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="d2c1a-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2c1a-134">輸入</span><span class="sxs-lookup"><span data-stu-id="d2c1a-134">INPUTS</span></span>

### <span data-ttu-id="d2c1a-135">PSStorageAccount 中的 [管理]。</span><span class="sxs-lookup"><span data-stu-id="d2c1a-135">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="d2c1a-136">System.object</span><span class="sxs-lookup"><span data-stu-id="d2c1a-136">System.String</span></span>

## <span data-ttu-id="d2c1a-137">輸出</span><span class="sxs-lookup"><span data-stu-id="d2c1a-137">OUTPUTS</span></span>

### <span data-ttu-id="d2c1a-138">PSRestorePolicy 中的 [管理]。</span><span class="sxs-lookup"><span data-stu-id="d2c1a-138">Microsoft.Azure.Commands.Management.Storage.Models.PSRestorePolicy</span></span>

## <span data-ttu-id="d2c1a-139">筆記</span><span class="sxs-lookup"><span data-stu-id="d2c1a-139">NOTES</span></span>

## <span data-ttu-id="d2c1a-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="d2c1a-140">RELATED LINKS</span></span>
