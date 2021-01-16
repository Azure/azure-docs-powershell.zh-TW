---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageobjectreplicationpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageObjectReplicationPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageObjectReplicationPolicy.md
ms.openlocfilehash: 6785eac6df5568f4b26e6de61ac0f4bfd8061259
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98280127"
---
# <span data-ttu-id="a6a61-101">Get-AzStorageObjectReplicationPolicy</span><span class="sxs-lookup"><span data-stu-id="a6a61-101">Get-AzStorageObjectReplicationPolicy</span></span>

## <span data-ttu-id="a6a61-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a6a61-102">SYNOPSIS</span></span>
<span data-ttu-id="a6a61-103">取得或列出儲存空間帳戶的物件複製原則。</span><span class="sxs-lookup"><span data-stu-id="a6a61-103">Gets or lists object replication policy of a Storage account.</span></span>

## <span data-ttu-id="a6a61-104">句法</span><span class="sxs-lookup"><span data-stu-id="a6a61-104">SYNTAX</span></span>

### <span data-ttu-id="a6a61-105">AccountName (預設) </span><span class="sxs-lookup"><span data-stu-id="a6a61-105">AccountName (Default)</span></span>
```
Get-AzStorageObjectReplicationPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 [-PolicyId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a6a61-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="a6a61-106">AccountObject</span></span>
```
Get-AzStorageObjectReplicationPolicy -StorageAccount <PSStorageAccount> [-PolicyId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a6a61-107">說明</span><span class="sxs-lookup"><span data-stu-id="a6a61-107">DESCRIPTION</span></span>
<span data-ttu-id="a6a61-108">**AzStorageObjectReplicationPolicy** Cmdlet 會取得或列出儲存空間帳戶的物件複製原則。</span><span class="sxs-lookup"><span data-stu-id="a6a61-108">The **Get-AzStorageObjectReplicationPolicy** cmdlet gets or lists object replication policy of a Storage account.</span></span>

## <span data-ttu-id="a6a61-109">示例</span><span class="sxs-lookup"><span data-stu-id="a6a61-109">EXAMPLES</span></span>

### <span data-ttu-id="a6a61-110">範例1：使用特定原則識別碼取得物件複製原則，並顯示其規則。</span><span class="sxs-lookup"><span data-stu-id="a6a61-110">Example 1: Get an object replication policy with specific policy Id and show its rules.</span></span>
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

<span data-ttu-id="a6a61-111">這個命令會取得具有特定原則識別碼的物件複製原則，並顯示其規則。</span><span class="sxs-lookup"><span data-stu-id="a6a61-111">This command gets an object replication policy with specific policy Id and show its rules.</span></span>

### <span data-ttu-id="a6a61-112">範例2：從儲存空間帳戶清單物件複製原則</span><span class="sxs-lookup"><span data-stu-id="a6a61-112">Example 2:List object replication policy from a Storage account</span></span>
```
PS C:\> $policies = Get-AzStorageObjectReplicationPolicy -ResourceGroupName "myresourcegroup" -AccountName "mydestaccount" 

PS C:\> $policies

ResourceGroupName StorageAccountName PolicyId                             EnabledTime SourceAccount   DestinationAccount Rules                                     
----------------- ------------------ --------                             ----------- -------------   ------------------ -----   
myresourcegroup   mydestaccount      56bfa11c-81ef-4f8d-b307-5e5386e16fba             mysrcaccount1   mydestaccount      [5fa8b1d6-4985-4abd-a0b3-ec4d07295a43,...]
myresourcegroup   mydestaccount      68434c7a-20d0-4282-b75c-43b5a243435e             mysrcaccount2   mydestaccount      [d3d39a01-8d92-40e5-849f-e56209ae5cf5,...]
```

<span data-ttu-id="a6a61-113">這個命令會列出儲存空間帳戶的物件複製原則。</span><span class="sxs-lookup"><span data-stu-id="a6a61-113">This command lists object replication policy from a Storage account.</span></span>

## <span data-ttu-id="a6a61-114">參數</span><span class="sxs-lookup"><span data-stu-id="a6a61-114">PARAMETERS</span></span>

### <span data-ttu-id="a6a61-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6a61-115">-DefaultProfile</span></span>
<span data-ttu-id="a6a61-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a6a61-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a6a61-117">-PolicyId</span><span class="sxs-lookup"><span data-stu-id="a6a61-117">-PolicyId</span></span>
<span data-ttu-id="a6a61-118">物件複製原則識別碼。</span><span class="sxs-lookup"><span data-stu-id="a6a61-118">Object Replication Policy Id.</span></span>

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

### <span data-ttu-id="a6a61-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a6a61-119">-ResourceGroupName</span></span>
<span data-ttu-id="a6a61-120">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="a6a61-120">Resource Group Name.</span></span>

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

### <span data-ttu-id="a6a61-121">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="a6a61-121">-StorageAccount</span></span>
<span data-ttu-id="a6a61-122">儲存空間帳戶物件</span><span class="sxs-lookup"><span data-stu-id="a6a61-122">Storage account object</span></span>

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

### <span data-ttu-id="a6a61-123">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="a6a61-123">-StorageAccountName</span></span>
<span data-ttu-id="a6a61-124">儲存空間帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="a6a61-124">Storage Account Name.</span></span>

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

### <span data-ttu-id="a6a61-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6a61-125">CommonParameters</span></span>
<span data-ttu-id="a6a61-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a6a61-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6a61-127">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="a6a61-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6a61-128">輸入</span><span class="sxs-lookup"><span data-stu-id="a6a61-128">INPUTS</span></span>

### <span data-ttu-id="a6a61-129">PSStorageAccount 中的 [管理]。</span><span class="sxs-lookup"><span data-stu-id="a6a61-129">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="a6a61-130">輸出</span><span class="sxs-lookup"><span data-stu-id="a6a61-130">OUTPUTS</span></span>

### <span data-ttu-id="a6a61-131">PSObjectReplicationPolicy 中的 [管理]。</span><span class="sxs-lookup"><span data-stu-id="a6a61-131">Microsoft.Azure.Commands.Management.Storage.Models.PSObjectReplicationPolicy</span></span>

## <span data-ttu-id="a6a61-132">筆記</span><span class="sxs-lookup"><span data-stu-id="a6a61-132">NOTES</span></span>

## <span data-ttu-id="a6a61-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="a6a61-133">RELATED LINKS</span></span>
