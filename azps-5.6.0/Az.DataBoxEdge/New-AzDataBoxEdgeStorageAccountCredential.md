---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/powershell/module/az.databoxedge/new-azdataboxedgestorageaccountcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeStorageAccountCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeStorageAccountCredential.md
ms.openlocfilehash: 23fe08b273b95cd5ad3866437d131f432e6cee38
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101908569"
---
# <span data-ttu-id="6bfa4-101">New-AzDataBoxEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="6bfa4-101">New-AzDataBoxEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="6bfa4-102">簡介</span><span class="sxs-lookup"><span data-stu-id="6bfa4-102">SYNOPSIS</span></span>
<span data-ttu-id="6bfa4-103">為裝置上的邊緣儲存空間帳戶建立新認證。</span><span class="sxs-lookup"><span data-stu-id="6bfa4-103">Creates new credentials for an edge storage account on the device.</span></span>

## <span data-ttu-id="6bfa4-104">語法</span><span class="sxs-lookup"><span data-stu-id="6bfa4-104">SYNTAX</span></span>

```
New-AzDataBoxEdgeStorageAccountCredential [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -StorageAccountType <String> -StorageAccountAccessKey <SecureString> -EncryptionKey <SecureString> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6bfa4-105">描述</span><span class="sxs-lookup"><span data-stu-id="6bfa4-105">DESCRIPTION</span></span>
<span data-ttu-id="6bfa4-106">**New-AzDataBoxEdgeStorageAccountCredential Cmdlet** 會為 Data Box Edge 裝置建立新的邊緣儲存空間帳號憑證。</span><span class="sxs-lookup"><span data-stu-id="6bfa4-106">The **New-AzDataBoxEdgeStorageAccountCredential** cmdlet creates a new edge storage account credential for a Data Box Edge device.</span></span>

## <span data-ttu-id="6bfa4-107">例子</span><span class="sxs-lookup"><span data-stu-id="6bfa4-107">EXAMPLES</span></span>

### <span data-ttu-id="6bfa4-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="6bfa4-108">Example 1</span></span>
```powershell
PS C:\> New-AzDataBoxEdgeStorageAccountCredential -ResourceGroupName resourceGroupName -DeviceName device-name -Name storage-acount-credential-name -StorageAccountName storageAccountName -StorageAccountType BlobStorage -StorageAccountAccessKey @SecureString -EncryptionKey @SecureString
Name                             StorageAccount    SslStatus  ResourceGroupName
--------------------------- ---------------------- ---------- ---------------------
storageAccountCredentalName storageAccountName     Enabled    resourceGroupName
```

## <span data-ttu-id="6bfa4-109">參數</span><span class="sxs-lookup"><span data-stu-id="6bfa4-109">PARAMETERS</span></span>

### <span data-ttu-id="6bfa4-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6bfa4-110">-AsJob</span></span>
<span data-ttu-id="6bfa4-111">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="6bfa4-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6bfa4-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6bfa4-112">-DefaultProfile</span></span>
<span data-ttu-id="6bfa4-113">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="6bfa4-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6bfa4-114">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="6bfa4-114">-DeviceName</span></span>
<span data-ttu-id="6bfa4-115">裝置名稱</span><span class="sxs-lookup"><span data-stu-id="6bfa4-115">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6bfa4-116">-EncryptionKey</span><span class="sxs-lookup"><span data-stu-id="6bfa4-116">-EncryptionKey</span></span>
<span data-ttu-id="6bfa4-117">Edge 裝置加密金鑰</span><span class="sxs-lookup"><span data-stu-id="6bfa4-117">Encryption key of the Edge device</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6bfa4-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="6bfa4-118">-Name</span></span>
<span data-ttu-id="6bfa4-119">要使用的儲存空間帳戶名稱</span><span class="sxs-lookup"><span data-stu-id="6bfa4-119">Name of the storage account to be used</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6bfa4-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6bfa4-120">-ResourceGroupName</span></span>
<span data-ttu-id="6bfa4-121">資源組名</span><span class="sxs-lookup"><span data-stu-id="6bfa4-121">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6bfa4-122">-StorageAccountAccessKey</span><span class="sxs-lookup"><span data-stu-id="6bfa4-122">-StorageAccountAccessKey</span></span>
<span data-ttu-id="6bfa4-123">提供儲存空間帳戶訪問金鑰</span><span class="sxs-lookup"><span data-stu-id="6bfa4-123">provide storage account access key</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6bfa4-124">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="6bfa4-124">-StorageAccountType</span></span>
<span data-ttu-id="6bfa4-125">可能的儲存存取類型 GeneralPurposeStorage， BlockStorage</span><span class="sxs-lookup"><span data-stu-id="6bfa4-125">Possible Storage Access type GeneralPurposeStorage, BlockStorage</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6bfa4-126">-確認</span><span class="sxs-lookup"><span data-stu-id="6bfa4-126">-Confirm</span></span>
<span data-ttu-id="6bfa4-127">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="6bfa4-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6bfa4-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6bfa4-128">-WhatIf</span></span>
<span data-ttu-id="6bfa4-129">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="6bfa4-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6bfa4-130">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6bfa4-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6bfa4-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6bfa4-131">CommonParameters</span></span>
<span data-ttu-id="6bfa4-132">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="6bfa4-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6bfa4-133">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6bfa4-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6bfa4-134">輸入</span><span class="sxs-lookup"><span data-stu-id="6bfa4-134">INPUTS</span></span>

### <span data-ttu-id="6bfa4-135">沒有</span><span class="sxs-lookup"><span data-stu-id="6bfa4-135">None</span></span>

## <span data-ttu-id="6bfa4-136">輸出</span><span class="sxs-lookup"><span data-stu-id="6bfa4-136">OUTPUTS</span></span>

### <span data-ttu-id="6bfa4-137">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDBoxEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="6bfa4-137">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="6bfa4-138">筆記</span><span class="sxs-lookup"><span data-stu-id="6bfa4-138">NOTES</span></span>

## <span data-ttu-id="6bfa4-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="6bfa4-139">RELATED LINKS</span></span>
