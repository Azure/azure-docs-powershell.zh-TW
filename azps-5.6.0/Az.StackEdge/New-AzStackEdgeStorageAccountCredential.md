---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/powershell/module/az.stackedge/new-azstackedgestorageaccountcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeStorageAccountCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeStorageAccountCredential.md
ms.openlocfilehash: a9bb0e844101c4d21db52c2f7852e3b548d283cc
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101915185"
---
# <span data-ttu-id="d9bdf-101">New-AzStackEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="d9bdf-101">New-AzStackEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="d9bdf-102">簡介</span><span class="sxs-lookup"><span data-stu-id="d9bdf-102">SYNOPSIS</span></span>
<span data-ttu-id="d9bdf-103">為裝置上的邊緣儲存空間帳戶建立新認證。</span><span class="sxs-lookup"><span data-stu-id="d9bdf-103">Creates new credentials for an edge storage account on the device.</span></span>

## <span data-ttu-id="d9bdf-104">語法</span><span class="sxs-lookup"><span data-stu-id="d9bdf-104">SYNTAX</span></span>

```
New-AzStackEdgeStorageAccountCredential [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -StorageAccountType <String> -StorageAccountAccessKey <SecureString> -EncryptionKey <SecureString> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d9bdf-105">描述</span><span class="sxs-lookup"><span data-stu-id="d9bdf-105">DESCRIPTION</span></span>
<span data-ttu-id="d9bdf-106">**New-AzStackEdgeStorageAccountCredential Cmdlet** 會為 Stack Edge 裝置建立新的邊緣儲存空間帳號憑證。</span><span class="sxs-lookup"><span data-stu-id="d9bdf-106">The **New-AzStackEdgeStorageAccountCredential** cmdlet creates a new edge storage account credential for a Stack Edge device.</span></span>

## <span data-ttu-id="d9bdf-107">例子</span><span class="sxs-lookup"><span data-stu-id="d9bdf-107">EXAMPLES</span></span>

### <span data-ttu-id="d9bdf-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="d9bdf-108">Example 1</span></span>
```powershell
PS C:\> New-AzStackEdgeStorageAccountCredential -ResourceGroupName resourceGroupName -DeviceName device-name -Name storage-acount-credential-name -StorageAccountName storageAccountName -StorageAccountType BlobStorage -StorageAccountAccessKey @SecureString -EncryptionKey @SecureString
Name                             StorageAccount    SslStatus  ResourceGroupName
--------------------------- ---------------------- ---------- ---------------------
storageAccountCredentalName storageAccountName     Enabled    resourceGroupName
```

## <span data-ttu-id="d9bdf-109">參數</span><span class="sxs-lookup"><span data-stu-id="d9bdf-109">PARAMETERS</span></span>

### <span data-ttu-id="d9bdf-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d9bdf-110">-AsJob</span></span>
<span data-ttu-id="d9bdf-111">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="d9bdf-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d9bdf-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9bdf-112">-DefaultProfile</span></span>
<span data-ttu-id="d9bdf-113">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="d9bdf-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d9bdf-114">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="d9bdf-114">-DeviceName</span></span>
<span data-ttu-id="d9bdf-115">裝置名稱</span><span class="sxs-lookup"><span data-stu-id="d9bdf-115">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d9bdf-116">-EncryptionKey</span><span class="sxs-lookup"><span data-stu-id="d9bdf-116">-EncryptionKey</span></span>
<span data-ttu-id="d9bdf-117">Edge 裝置加密金鑰</span><span class="sxs-lookup"><span data-stu-id="d9bdf-117">Encryption key of the Edge device</span></span>

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

### <span data-ttu-id="d9bdf-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="d9bdf-118">-Name</span></span>
<span data-ttu-id="d9bdf-119">要使用的儲存空間帳戶名稱</span><span class="sxs-lookup"><span data-stu-id="d9bdf-119">Name of the storage account to be used</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountCredentialName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d9bdf-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d9bdf-120">-ResourceGroupName</span></span>
<span data-ttu-id="d9bdf-121">資源組名</span><span class="sxs-lookup"><span data-stu-id="d9bdf-121">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d9bdf-122">-StorageAccountAccessKey</span><span class="sxs-lookup"><span data-stu-id="d9bdf-122">-StorageAccountAccessKey</span></span>
<span data-ttu-id="d9bdf-123">提供儲存空間帳戶訪問金鑰</span><span class="sxs-lookup"><span data-stu-id="d9bdf-123">provide storage account access key</span></span>

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

### <span data-ttu-id="d9bdf-124">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="d9bdf-124">-StorageAccountType</span></span>
<span data-ttu-id="d9bdf-125">可能的儲存存取類型 GeneralPurposeStorage， BlockStorage</span><span class="sxs-lookup"><span data-stu-id="d9bdf-125">Possible Storage Access type GeneralPurposeStorage, BlockStorage</span></span>

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

### <span data-ttu-id="d9bdf-126">-確認</span><span class="sxs-lookup"><span data-stu-id="d9bdf-126">-Confirm</span></span>
<span data-ttu-id="d9bdf-127">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="d9bdf-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d9bdf-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d9bdf-128">-WhatIf</span></span>
<span data-ttu-id="d9bdf-129">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="d9bdf-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d9bdf-130">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d9bdf-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d9bdf-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9bdf-131">CommonParameters</span></span>
<span data-ttu-id="d9bdf-132">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="d9bdf-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9bdf-133">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d9bdf-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9bdf-134">輸入</span><span class="sxs-lookup"><span data-stu-id="d9bdf-134">INPUTS</span></span>

### <span data-ttu-id="d9bdf-135">沒有</span><span class="sxs-lookup"><span data-stu-id="d9bdf-135">None</span></span>

## <span data-ttu-id="d9bdf-136">輸出</span><span class="sxs-lookup"><span data-stu-id="d9bdf-136">OUTPUTS</span></span>

### <span data-ttu-id="d9bdf-137">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.models.PSStackEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="d9bdf-137">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="d9bdf-138">筆記</span><span class="sxs-lookup"><span data-stu-id="d9bdf-138">NOTES</span></span>

## <span data-ttu-id="d9bdf-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="d9bdf-139">RELATED LINKS</span></span>
