---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/get-aznetappfilesbackuppolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesBackupPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesBackupPolicy.md
ms.openlocfilehash: 754149172b3154975580a0802426f9a2f20c0f62
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98435260"
---
# <span data-ttu-id="6a7ef-101">Get-AzNetAppFilesBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="6a7ef-101">Get-AzNetAppFilesBackupPolicy</span></span>

## <span data-ttu-id="6a7ef-102">摘要</span><span class="sxs-lookup"><span data-stu-id="6a7ef-102">SYNOPSIS</span></span>
<span data-ttu-id="6a7ef-103">取得 (ANF) 備份原則的 Azure NetApp 檔案的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="6a7ef-103">Gets details of an Azure NetApp Files (ANF) Backup Policy.</span></span>

## <span data-ttu-id="6a7ef-104">句法</span><span class="sxs-lookup"><span data-stu-id="6a7ef-104">SYNTAX</span></span>

### <span data-ttu-id="6a7ef-105">ByFieldsParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="6a7ef-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzNetAppFilesBackupPolicy -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6a7ef-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6a7ef-106">ByResourceIdParameterSet</span></span>
```
Get-AzNetAppFilesBackupPolicy [-Name <String>] -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6a7ef-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6a7ef-107">ByParentObjectParameterSet</span></span>
```
Get-AzNetAppFilesBackupPolicy [-Name <String>] -AccountObject <PSNetAppFilesAccount>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6a7ef-108">說明</span><span class="sxs-lookup"><span data-stu-id="6a7ef-108">DESCRIPTION</span></span>
<span data-ttu-id="6a7ef-109">**AzNetAppFilesBackupPolicy** Cmdlet 會取得 ANF 備份原則的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="6a7ef-109">The **Get-AzNetAppFilesBackupPolicy** cmdlet gets details of an ANF backup policy.</span></span>

## <span data-ttu-id="6a7ef-110">示例</span><span class="sxs-lookup"><span data-stu-id="6a7ef-110">EXAMPLES</span></span>

### <span data-ttu-id="6a7ef-111">範例1</span><span class="sxs-lookup"><span data-stu-id="6a7ef-111">Example 1</span></span>
```powershell
PS C:\> Get-AzNetAppFilesBackupPolicy -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -Name "MyBackupPolicy"
```

<span data-ttu-id="6a7ef-112">這個命令會取得帳戶「MyAnfAccount」的名為「MyBackupPolicy」的備份原則。</span><span class="sxs-lookup"><span data-stu-id="6a7ef-112">This command gets the backup policy named "MyBackupPolicy" for account "MyAnfAccount".</span></span>

## <span data-ttu-id="6a7ef-113">參數</span><span class="sxs-lookup"><span data-stu-id="6a7ef-113">PARAMETERS</span></span>

### <span data-ttu-id="6a7ef-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="6a7ef-114">-AccountName</span></span>
<span data-ttu-id="6a7ef-115">ANF 帳戶的名稱</span><span class="sxs-lookup"><span data-stu-id="6a7ef-115">The name of the ANF account</span></span>

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

### <span data-ttu-id="6a7ef-116">-AccountObject</span><span class="sxs-lookup"><span data-stu-id="6a7ef-116">-AccountObject</span></span>
<span data-ttu-id="6a7ef-117">包含要傳回之備份原則的帳戶物件</span><span class="sxs-lookup"><span data-stu-id="6a7ef-117">The Account object containing the Backup Policy to return</span></span>

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

### <span data-ttu-id="6a7ef-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a7ef-118">-DefaultProfile</span></span>
<span data-ttu-id="6a7ef-119">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="6a7ef-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6a7ef-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="6a7ef-120">-Name</span></span>
<span data-ttu-id="6a7ef-121">ANF 備份原則的名稱</span><span class="sxs-lookup"><span data-stu-id="6a7ef-121">The name of the ANF backup policy</span></span>

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

### <span data-ttu-id="6a7ef-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6a7ef-122">-ResourceGroupName</span></span>
<span data-ttu-id="6a7ef-123">ANF 帳戶的 [資源] 群組</span><span class="sxs-lookup"><span data-stu-id="6a7ef-123">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="6a7ef-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6a7ef-124">-ResourceId</span></span>
<span data-ttu-id="6a7ef-125">ANF 備份原則的資源識別碼</span><span class="sxs-lookup"><span data-stu-id="6a7ef-125">The resource id of the ANF Backup Policy</span></span>

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

### <span data-ttu-id="6a7ef-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a7ef-126">CommonParameters</span></span>
<span data-ttu-id="6a7ef-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="6a7ef-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a7ef-128">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="6a7ef-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a7ef-129">輸入</span><span class="sxs-lookup"><span data-stu-id="6a7ef-129">INPUTS</span></span>

### <span data-ttu-id="6a7ef-130">System.object</span><span class="sxs-lookup"><span data-stu-id="6a7ef-130">System.String</span></span>

### <span data-ttu-id="6a7ef-131">PSNetAppFilesAccount 中的 NetAppFiles。</span><span class="sxs-lookup"><span data-stu-id="6a7ef-131">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="6a7ef-132">輸出</span><span class="sxs-lookup"><span data-stu-id="6a7ef-132">OUTPUTS</span></span>

### <span data-ttu-id="6a7ef-133">PSNetAppFilesBackupPolicy 中的 NetAppFiles。</span><span class="sxs-lookup"><span data-stu-id="6a7ef-133">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackupPolicy</span></span>

## <span data-ttu-id="6a7ef-134">筆記</span><span class="sxs-lookup"><span data-stu-id="6a7ef-134">NOTES</span></span>

## <span data-ttu-id="6a7ef-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="6a7ef-135">RELATED LINKS</span></span>
