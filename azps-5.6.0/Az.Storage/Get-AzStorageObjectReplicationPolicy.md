---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/az.storage/get-azstorageobjectreplicationpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageObjectReplicationPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageObjectReplicationPolicy.md
ms.openlocfilehash: 00d88c594d1f36c01bb47e7b392dcdd2ebeb2774
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101909293"
---
# <span data-ttu-id="5026a-101">Get-AzStorageObjectReplicationPolicy</span><span class="sxs-lookup"><span data-stu-id="5026a-101">Get-AzStorageObjectReplicationPolicy</span></span>

## <span data-ttu-id="5026a-102">簡介</span><span class="sxs-lookup"><span data-stu-id="5026a-102">SYNOPSIS</span></span>
<span data-ttu-id="5026a-103">獲取或列出儲存空間帳戶的物件複寫原則。</span><span class="sxs-lookup"><span data-stu-id="5026a-103">Gets or lists object replication policy of a Storage account.</span></span>

## <span data-ttu-id="5026a-104">語法</span><span class="sxs-lookup"><span data-stu-id="5026a-104">SYNTAX</span></span>

### <span data-ttu-id="5026a-105">AccountName (預設) </span><span class="sxs-lookup"><span data-stu-id="5026a-105">AccountName (Default)</span></span>
```
Get-AzStorageObjectReplicationPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 [-PolicyId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5026a-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="5026a-106">AccountObject</span></span>
```
Get-AzStorageObjectReplicationPolicy -StorageAccount <PSStorageAccount> [-PolicyId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5026a-107">描述</span><span class="sxs-lookup"><span data-stu-id="5026a-107">DESCRIPTION</span></span>
<span data-ttu-id="5026a-108">**Get-AzStorageObjectReplicationPolicy** Cmdlet 取得或列出儲存帳戶的物件複寫原則。</span><span class="sxs-lookup"><span data-stu-id="5026a-108">The **Get-AzStorageObjectReplicationPolicy** cmdlet gets or lists object replication policy of a Storage account.</span></span>

## <span data-ttu-id="5026a-109">例子</span><span class="sxs-lookup"><span data-stu-id="5026a-109">EXAMPLES</span></span>

### <span data-ttu-id="5026a-110">範例 1：取得具有特定原則識別碼的物件複製原則，並顯示其規則。</span><span class="sxs-lookup"><span data-stu-id="5026a-110">Example 1: Get an object replication policy with specific policy Id and show its rules.</span></span>
```
PS C:\> $policy = Get-AzStorageObjectReplicationPolicy -ResourceGroupName "myresourcegroup" -AccountName "mydestaccount" -PolicyId 56bfa11c-81ef-4f8d-b307-5e5386e16fba

PS C:\> $policy

ResourceGroupName StorageAccountName PolicyId                             EnabledTime SourceAccount   DestinationAccount Rules                                     
----------------- ------------------ --------                             ----------- -------------   ------------------ -----   
myresourcegroup   mydestaccount      56bfa11c-81ef-4f8d-b307-5e5386e16fba             mysourceaccount mydestaccount      [5fa8b1d6-4985-4abd-a0b3-ec4d07295a43,...]

PS C:\> $policy.Rules

RuleId                               SourceContainer DestinationContainer Filters.PrefixMatch Filters.MinCreationTime
------                               --------------- -------------------- ------------------- -----------------------
d3d39a01-8d92-40e5-849f-e56209ae5cf5 src1            dest1                {}                                         
2407de9a-3301-4656-858f-359d185565e0 src             dest                 {a, abc, dd}        2019-01-01T16:00:00Z
```

<span data-ttu-id="5026a-111">此命令會獲得具有特定原則識別碼的物件複製原則，並顯示其規則。</span><span class="sxs-lookup"><span data-stu-id="5026a-111">This command gets an object replication policy with specific policy Id and show its rules.</span></span>

### <span data-ttu-id="5026a-112">範例 2：從儲存空間帳戶列出物件複寫原則</span><span class="sxs-lookup"><span data-stu-id="5026a-112">Example 2:List object replication policy from a Storage account</span></span>
```
PS C:\> $policies = Get-AzStorageObjectReplicationPolicy -ResourceGroupName "myresourcegroup" -AccountName "mydestaccount" 

PS C:\> $policies

ResourceGroupName StorageAccountName PolicyId                             EnabledTime SourceAccount   DestinationAccount Rules                                     
----------------- ------------------ --------                             ----------- -------------   ------------------ -----   
myresourcegroup   mydestaccount      56bfa11c-81ef-4f8d-b307-5e5386e16fba             mysrcaccount1   mydestaccount      [5fa8b1d6-4985-4abd-a0b3-ec4d07295a43,...]
myresourcegroup   mydestaccount      68434c7a-20d0-4282-b75c-43b5a243435e             mysrcaccount2   mydestaccount      [d3d39a01-8d92-40e5-849f-e56209ae5cf5,...]
```

<span data-ttu-id="5026a-113">此命令會列出來自儲存空間帳戶的物件複寫原則。</span><span class="sxs-lookup"><span data-stu-id="5026a-113">This command lists object replication policy from a Storage account.</span></span>

## <span data-ttu-id="5026a-114">參數</span><span class="sxs-lookup"><span data-stu-id="5026a-114">PARAMETERS</span></span>

### <span data-ttu-id="5026a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5026a-115">-DefaultProfile</span></span>
<span data-ttu-id="5026a-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="5026a-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5026a-117">-PolicyId</span><span class="sxs-lookup"><span data-stu-id="5026a-117">-PolicyId</span></span>
<span data-ttu-id="5026a-118">物件複寫原則識別碼。</span><span class="sxs-lookup"><span data-stu-id="5026a-118">Object Replication Policy Id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5026a-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5026a-119">-ResourceGroupName</span></span>
<span data-ttu-id="5026a-120">資源組名。</span><span class="sxs-lookup"><span data-stu-id="5026a-120">Resource Group Name.</span></span>

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

### <span data-ttu-id="5026a-121">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="5026a-121">-StorageAccount</span></span>
<span data-ttu-id="5026a-122">儲存空間帳戶物件</span><span class="sxs-lookup"><span data-stu-id="5026a-122">Storage account object</span></span>

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

### <span data-ttu-id="5026a-123">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="5026a-123">-StorageAccountName</span></span>
<span data-ttu-id="5026a-124">儲存空間帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="5026a-124">Storage Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases: AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5026a-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5026a-125">CommonParameters</span></span>
<span data-ttu-id="5026a-126">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="5026a-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5026a-127">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="5026a-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5026a-128">輸入</span><span class="sxs-lookup"><span data-stu-id="5026a-128">INPUTS</span></span>

### <span data-ttu-id="5026a-129">Microsoft.Azure.Commands.management.storage.models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="5026a-129">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="5026a-130">輸出</span><span class="sxs-lookup"><span data-stu-id="5026a-130">OUTPUTS</span></span>

### <span data-ttu-id="5026a-131">Microsoft.Azure.Commands.management.storage.models.PSObjectReplicationPolicy</span><span class="sxs-lookup"><span data-stu-id="5026a-131">Microsoft.Azure.Commands.Management.Storage.Models.PSObjectReplicationPolicy</span></span>

## <span data-ttu-id="5026a-132">筆記</span><span class="sxs-lookup"><span data-stu-id="5026a-132">NOTES</span></span>

## <span data-ttu-id="5026a-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="5026a-133">RELATED LINKS</span></span>
