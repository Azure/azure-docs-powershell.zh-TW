---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/powershell/module/az.netappfiles/get-aznetappfilesbackuppolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesBackupPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesBackupPolicy.md
ms.openlocfilehash: fc8e3d49f5c5a6430a6436b0d46e8fd10984db98
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101906078"
---
# <span data-ttu-id="847b7-101">Get-AzNetAppFilesBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="847b7-101">Get-AzNetAppFilesBackupPolicy</span></span>

## <span data-ttu-id="847b7-102">簡介</span><span class="sxs-lookup"><span data-stu-id="847b7-102">SYNOPSIS</span></span>
<span data-ttu-id="847b7-103">在備份策略的 ANF 中 (Azure NetApp 檔案) 詳細資料。</span><span class="sxs-lookup"><span data-stu-id="847b7-103">Gets details of an Azure NetApp Files (ANF) Backup Policy.</span></span>

## <span data-ttu-id="847b7-104">語法</span><span class="sxs-lookup"><span data-stu-id="847b7-104">SYNTAX</span></span>

### <span data-ttu-id="847b7-105">ByFieldsParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="847b7-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzNetAppFilesBackupPolicy -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="847b7-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="847b7-106">ByResourceIdParameterSet</span></span>
```
Get-AzNetAppFilesBackupPolicy [-Name <String>] -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="847b7-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="847b7-107">ByParentObjectParameterSet</span></span>
```
Get-AzNetAppFilesBackupPolicy [-Name <String>] -AccountObject <PSNetAppFilesAccount>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="847b7-108">描述</span><span class="sxs-lookup"><span data-stu-id="847b7-108">DESCRIPTION</span></span>
<span data-ttu-id="847b7-109">**Get-AzNetAppFilesBackupPolicy** Cmdlet 會取得 ANF 備份策略的詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="847b7-109">The **Get-AzNetAppFilesBackupPolicy** cmdlet gets details of an ANF backup policy.</span></span>

## <span data-ttu-id="847b7-110">例子</span><span class="sxs-lookup"><span data-stu-id="847b7-110">EXAMPLES</span></span>

### <span data-ttu-id="847b7-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="847b7-111">Example 1</span></span>
```powershell
PS C:\> Get-AzNetAppFilesBackupPolicy -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -Name "MyBackupPolicy"
```

<span data-ttu-id="847b7-112">此命令會針對帳戶 「MyAnfAccount」，獲得名為「MyBackupPolicy」的備份策略。</span><span class="sxs-lookup"><span data-stu-id="847b7-112">This command gets the backup policy named "MyBackupPolicy" for account "MyAnfAccount".</span></span>

## <span data-ttu-id="847b7-113">參數</span><span class="sxs-lookup"><span data-stu-id="847b7-113">PARAMETERS</span></span>

### <span data-ttu-id="847b7-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="847b7-114">-AccountName</span></span>
<span data-ttu-id="847b7-115">ANF 帳戶的名稱</span><span class="sxs-lookup"><span data-stu-id="847b7-115">The name of the ANF account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="847b7-116">-AccountObject</span><span class="sxs-lookup"><span data-stu-id="847b7-116">-AccountObject</span></span>
<span data-ttu-id="847b7-117">包含要退回之備份策略的帳戶物件</span><span class="sxs-lookup"><span data-stu-id="847b7-117">The Account object containing the Backup Policy to return</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="847b7-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="847b7-118">-DefaultProfile</span></span>
<span data-ttu-id="847b7-119">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="847b7-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="847b7-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="847b7-120">-Name</span></span>
<span data-ttu-id="847b7-121">ANF 備份策略的名稱</span><span class="sxs-lookup"><span data-stu-id="847b7-121">The name of the ANF backup policy</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: BackupPolicyName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="847b7-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="847b7-122">-ResourceGroupName</span></span>
<span data-ttu-id="847b7-123">ANF 帳戶的資源群組</span><span class="sxs-lookup"><span data-stu-id="847b7-123">The resource group of the ANF account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="847b7-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="847b7-124">-ResourceId</span></span>
<span data-ttu-id="847b7-125">ANF 備份策略的資源識別碼</span><span class="sxs-lookup"><span data-stu-id="847b7-125">The resource id of the ANF Backup Policy</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="847b7-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="847b7-126">CommonParameters</span></span>
<span data-ttu-id="847b7-127">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="847b7-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="847b7-128">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="847b7-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="847b7-129">輸入</span><span class="sxs-lookup"><span data-stu-id="847b7-129">INPUTS</span></span>

### <span data-ttu-id="847b7-130">System.String</span><span class="sxs-lookup"><span data-stu-id="847b7-130">System.String</span></span>

### <span data-ttu-id="847b7-131">Microsoft.Azure.Commands.NetAppFiles.models.PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="847b7-131">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="847b7-132">輸出</span><span class="sxs-lookup"><span data-stu-id="847b7-132">OUTPUTS</span></span>

### <span data-ttu-id="847b7-133">Microsoft.Azure.Commands.NetAppFiles.models.PSNetAppFilesBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="847b7-133">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackupPolicy</span></span>

## <span data-ttu-id="847b7-134">筆記</span><span class="sxs-lookup"><span data-stu-id="847b7-134">NOTES</span></span>

## <span data-ttu-id="847b7-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="847b7-135">RELATED LINKS</span></span>
