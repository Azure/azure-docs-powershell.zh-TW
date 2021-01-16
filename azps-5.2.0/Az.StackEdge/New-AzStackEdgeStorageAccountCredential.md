---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/new-azstackedgestorageaccountcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeStorageAccountCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeStorageAccountCredential.md
ms.openlocfilehash: d4e9062b15e7d5ca7338e13cdcdf71506ba23e29
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98280575"
---
# <span data-ttu-id="eb3e5-101">New-AzStackEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="eb3e5-101">New-AzStackEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="eb3e5-102">摘要</span><span class="sxs-lookup"><span data-stu-id="eb3e5-102">SYNOPSIS</span></span>
<span data-ttu-id="eb3e5-103">為裝置上的 edge 儲存空間帳戶建立新的認證。</span><span class="sxs-lookup"><span data-stu-id="eb3e5-103">Creates new credentials for an edge storage account on the device.</span></span>

## <span data-ttu-id="eb3e5-104">句法</span><span class="sxs-lookup"><span data-stu-id="eb3e5-104">SYNTAX</span></span>

```
New-AzStackEdgeStorageAccountCredential [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -StorageAccountType <String> -StorageAccountAccessKey <SecureString> -EncryptionKey <SecureString> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eb3e5-105">說明</span><span class="sxs-lookup"><span data-stu-id="eb3e5-105">DESCRIPTION</span></span>
<span data-ttu-id="eb3e5-106">**新的-AzStackEdgeStorageAccountCredential** Cmdlet 會針對堆疊 edge 裝置建立新的 edge 儲存空間帳號憑證。</span><span class="sxs-lookup"><span data-stu-id="eb3e5-106">The **New-AzStackEdgeStorageAccountCredential** cmdlet creates a new edge storage account credential for a Stack Edge device.</span></span>

## <span data-ttu-id="eb3e5-107">示例</span><span class="sxs-lookup"><span data-stu-id="eb3e5-107">EXAMPLES</span></span>

### <span data-ttu-id="eb3e5-108">範例1</span><span class="sxs-lookup"><span data-stu-id="eb3e5-108">Example 1</span></span>
```powershell
PS C:\> New-AzStackEdgeStorageAccountCredential -ResourceGroupName resourceGroupName -DeviceName device-name -Name storage-acount-credential-name -StorageAccountName storageAccountName -StorageAccountType BlobStorage -StorageAccountAccessKey @SecureString -EncryptionKey @SecureString
Name                             StorageAccount    SslStatus  ResourceGroupName
--------------------------- ---------------------- ---------- ---------------------
storageAccountCredentalName storageAccountName     Enabled    resourceGroupName
```

## <span data-ttu-id="eb3e5-109">參數</span><span class="sxs-lookup"><span data-stu-id="eb3e5-109">PARAMETERS</span></span>

### <span data-ttu-id="eb3e5-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="eb3e5-110">-AsJob</span></span>
<span data-ttu-id="eb3e5-111">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="eb3e5-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="eb3e5-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eb3e5-112">-DefaultProfile</span></span>
<span data-ttu-id="eb3e5-113">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="eb3e5-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="eb3e5-114">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="eb3e5-114">-DeviceName</span></span>
<span data-ttu-id="eb3e5-115">裝置名稱</span><span class="sxs-lookup"><span data-stu-id="eb3e5-115">Device Name</span></span>

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

### <span data-ttu-id="eb3e5-116">-Encryption.encryptionkey</span><span class="sxs-lookup"><span data-stu-id="eb3e5-116">-EncryptionKey</span></span>
<span data-ttu-id="eb3e5-117">Edge 裝置的加密金鑰</span><span class="sxs-lookup"><span data-stu-id="eb3e5-117">Encryption key of the Edge device</span></span>

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

### <span data-ttu-id="eb3e5-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="eb3e5-118">-Name</span></span>
<span data-ttu-id="eb3e5-119">要使用的儲存空間帳戶名稱</span><span class="sxs-lookup"><span data-stu-id="eb3e5-119">Name of the storage account to be used</span></span>

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

### <span data-ttu-id="eb3e5-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eb3e5-120">-ResourceGroupName</span></span>
<span data-ttu-id="eb3e5-121">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="eb3e5-121">Resource Group Name</span></span>

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

### <span data-ttu-id="eb3e5-122">-StorageAccountAccessKey</span><span class="sxs-lookup"><span data-stu-id="eb3e5-122">-StorageAccountAccessKey</span></span>
<span data-ttu-id="eb3e5-123">提供儲存空間帳戶存取金鑰</span><span class="sxs-lookup"><span data-stu-id="eb3e5-123">provide storage account access key</span></span>

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

### <span data-ttu-id="eb3e5-124">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="eb3e5-124">-StorageAccountType</span></span>
<span data-ttu-id="eb3e5-125">可能的儲存存取類型 GeneralPurposeStorage、BlockStorage</span><span class="sxs-lookup"><span data-stu-id="eb3e5-125">Possible Storage Access type GeneralPurposeStorage, BlockStorage</span></span>

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

### <span data-ttu-id="eb3e5-126">-確認</span><span class="sxs-lookup"><span data-stu-id="eb3e5-126">-Confirm</span></span>
<span data-ttu-id="eb3e5-127">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="eb3e5-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eb3e5-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eb3e5-128">-WhatIf</span></span>
<span data-ttu-id="eb3e5-129">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="eb3e5-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="eb3e5-130">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="eb3e5-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eb3e5-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb3e5-131">CommonParameters</span></span>
<span data-ttu-id="eb3e5-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="eb3e5-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb3e5-133">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="eb3e5-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb3e5-134">輸入</span><span class="sxs-lookup"><span data-stu-id="eb3e5-134">INPUTS</span></span>

### <span data-ttu-id="eb3e5-135">所有</span><span class="sxs-lookup"><span data-stu-id="eb3e5-135">None</span></span>

## <span data-ttu-id="eb3e5-136">輸出</span><span class="sxs-lookup"><span data-stu-id="eb3e5-136">OUTPUTS</span></span>

### <span data-ttu-id="eb3e5-137">PSStackEdgeStorageAccountCredential （StackEdge）的</span><span class="sxs-lookup"><span data-stu-id="eb3e5-137">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="eb3e5-138">筆記</span><span class="sxs-lookup"><span data-stu-id="eb3e5-138">NOTES</span></span>

## <span data-ttu-id="eb3e5-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="eb3e5-139">RELATED LINKS</span></span>
