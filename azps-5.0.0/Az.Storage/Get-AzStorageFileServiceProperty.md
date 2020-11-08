---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstoragefileserviceproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageFileServiceProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageFileServiceProperty.md
ms.openlocfilehash: 0824045a6b916d34a7b268c32e9667e954a4e1e5
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94137794"
---
# <span data-ttu-id="fbf31-101">Get-AzStorageFileServiceProperty</span><span class="sxs-lookup"><span data-stu-id="fbf31-101">Get-AzStorageFileServiceProperty</span></span>

## <span data-ttu-id="fbf31-102">摘要</span><span class="sxs-lookup"><span data-stu-id="fbf31-102">SYNOPSIS</span></span>
<span data-ttu-id="fbf31-103">取得 Azure 儲存空間服務的服務屬性。</span><span class="sxs-lookup"><span data-stu-id="fbf31-103">Gets service properties for Azure Storage File services.</span></span>

## <span data-ttu-id="fbf31-104">句法</span><span class="sxs-lookup"><span data-stu-id="fbf31-104">SYNTAX</span></span>

### <span data-ttu-id="fbf31-105">AccountName (預設) </span><span class="sxs-lookup"><span data-stu-id="fbf31-105">AccountName (Default)</span></span>
```
Get-AzStorageFileServiceProperty [-ResourceGroupName] <String> [-StorageAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fbf31-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="fbf31-106">AccountObject</span></span>
```
Get-AzStorageFileServiceProperty -StorageAccount <PSStorageAccount> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="fbf31-107">FileServicePropertiesResourceId</span><span class="sxs-lookup"><span data-stu-id="fbf31-107">FileServicePropertiesResourceId</span></span>
```
Get-AzStorageFileServiceProperty [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="fbf31-108">說明</span><span class="sxs-lookup"><span data-stu-id="fbf31-108">DESCRIPTION</span></span>
<span data-ttu-id="fbf31-109">**AzStorageFileServiceProperty** Cmdlet 會取得 Azure Storage 檔服務的服務屬性。</span><span class="sxs-lookup"><span data-stu-id="fbf31-109">The **Get-AzStorageFileServiceProperty** cmdlet gets the service properties for Azure Storage File services.</span></span>

## <span data-ttu-id="fbf31-110">示例</span><span class="sxs-lookup"><span data-stu-id="fbf31-110">EXAMPLES</span></span>

### <span data-ttu-id="fbf31-111">範例1：取得指定儲存空間帳戶的 Azure 儲存空間服務屬性</span><span class="sxs-lookup"><span data-stu-id="fbf31-111">Example 1: Get  Azure Storage File services property of a specified Storage Account</span></span>
```powershell
PS C:\> Get-AzStorageFileServiceProperty -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount"

StorageAccountName ResourceGroupName ShareDeleteRetentionPolicy.Enabled ShareDeleteRetentionPolicy.Days
------------------ ----------------- ---------------------------------- -------------------------------
mystorageaccount   myresourcegroup   True                               5
```

<span data-ttu-id="fbf31-112">這個命令會取得指定儲存空間帳戶的 [檔案服務] 屬性。</span><span class="sxs-lookup"><span data-stu-id="fbf31-112">This command gets the File services property of a specified Storage Account.</span></span>

## <span data-ttu-id="fbf31-113">參數</span><span class="sxs-lookup"><span data-stu-id="fbf31-113">PARAMETERS</span></span>

### <span data-ttu-id="fbf31-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fbf31-114">-DefaultProfile</span></span>
<span data-ttu-id="fbf31-115">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="fbf31-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fbf31-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fbf31-116">-ResourceGroupName</span></span>
<span data-ttu-id="fbf31-117">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="fbf31-117">Resource Group Name.</span></span>

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

### <span data-ttu-id="fbf31-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fbf31-118">-ResourceId</span></span>
<span data-ttu-id="fbf31-119">輸入儲存空間帳戶資源識別碼，或 [檔案服務] 屬性 [資源識別碼]。</span><span class="sxs-lookup"><span data-stu-id="fbf31-119">Input a Storage account Resource Id, or a File service properties Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: FileServicePropertiesResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fbf31-120">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="fbf31-120">-StorageAccount</span></span>
<span data-ttu-id="fbf31-121">儲存空間帳戶物件</span><span class="sxs-lookup"><span data-stu-id="fbf31-121">Storage account object</span></span>

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

### <span data-ttu-id="fbf31-122">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="fbf31-122">-StorageAccountName</span></span>
<span data-ttu-id="fbf31-123">儲存空間帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="fbf31-123">Storage Account Name.</span></span>

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

### <span data-ttu-id="fbf31-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fbf31-124">CommonParameters</span></span>
<span data-ttu-id="fbf31-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="fbf31-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fbf31-126">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="fbf31-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fbf31-127">輸入</span><span class="sxs-lookup"><span data-stu-id="fbf31-127">INPUTS</span></span>

### <span data-ttu-id="fbf31-128">PSStorageAccount 中的 [管理]。</span><span class="sxs-lookup"><span data-stu-id="fbf31-128">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="fbf31-129">System.object</span><span class="sxs-lookup"><span data-stu-id="fbf31-129">System.String</span></span>

## <span data-ttu-id="fbf31-130">輸出</span><span class="sxs-lookup"><span data-stu-id="fbf31-130">OUTPUTS</span></span>

### <span data-ttu-id="fbf31-131">PSFileServiceProperties 中的 [管理]。</span><span class="sxs-lookup"><span data-stu-id="fbf31-131">Microsoft.Azure.Commands.Management.Storage.Models.PSFileServiceProperties</span></span>

## <span data-ttu-id="fbf31-132">筆記</span><span class="sxs-lookup"><span data-stu-id="fbf31-132">NOTES</span></span>

## <span data-ttu-id="fbf31-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="fbf31-133">RELATED LINKS</span></span>