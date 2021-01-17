---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/get-aznetappfilesvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesVault.md
ms.openlocfilehash: 9779db097028710aa8aeddc7a5a1c5bdea85a30a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98435253"
---
# <span data-ttu-id="b88c7-101">Get-AzNetAppFilesVault</span><span class="sxs-lookup"><span data-stu-id="b88c7-101">Get-AzNetAppFilesVault</span></span>

## <span data-ttu-id="b88c7-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b88c7-102">SYNOPSIS</span></span>
<span data-ttu-id="b88c7-103">取得 (ANF) 帳戶備份電子倉庫的 Azure NetApp 檔案清單。</span><span class="sxs-lookup"><span data-stu-id="b88c7-103">Gets list of Azure NetApp Files (ANF) Accounts backup vaults.</span></span>

## <span data-ttu-id="b88c7-104">句法</span><span class="sxs-lookup"><span data-stu-id="b88c7-104">SYNTAX</span></span>

### <span data-ttu-id="b88c7-105">ByFieldsParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="b88c7-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzNetAppFilesVault -ResourceGroupName <String> [-AccountName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b88c7-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b88c7-106">ByParentObjectParameterSet</span></span>
```
Get-AzNetAppFilesVault -AccountObject <PSNetAppFilesAccount> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b88c7-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b88c7-107">ByResourceIdParameterSet</span></span>
```
Get-AzNetAppFilesVault -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b88c7-108">說明</span><span class="sxs-lookup"><span data-stu-id="b88c7-108">DESCRIPTION</span></span>
<span data-ttu-id="b88c7-109">**AzNetAppFilesVault** Cmdlet 會取得 ANF 帳戶備份電子倉庫的清單。</span><span class="sxs-lookup"><span data-stu-id="b88c7-109">The **Get-AzNetAppFilesVault** cmdlet gets list of an ANF accounts backup vaults.</span></span>

## <span data-ttu-id="b88c7-110">示例</span><span class="sxs-lookup"><span data-stu-id="b88c7-110">EXAMPLES</span></span>

### <span data-ttu-id="b88c7-111">範例1</span><span class="sxs-lookup"><span data-stu-id="b88c7-111">Example 1</span></span>
```powershell
PS C:\> Get-AzNetAppFilesVault -ResourceGroupName "MyRG" -AccountName "MyAnfAccount"
```

<span data-ttu-id="b88c7-112">這個命令會取得 Azure NetappFiles 的備份保存庫清單 (ANF) 帳戶 "MyAnfAccount"。</span><span class="sxs-lookup"><span data-stu-id="b88c7-112">This command gets a list of the backup vaults for Azure NetappFiles (ANF) account "MyAnfAccount".</span></span>

## <span data-ttu-id="b88c7-113">參數</span><span class="sxs-lookup"><span data-stu-id="b88c7-113">PARAMETERS</span></span>

### <span data-ttu-id="b88c7-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="b88c7-114">-AccountName</span></span>
<span data-ttu-id="b88c7-115">ANF 帳戶的名稱</span><span class="sxs-lookup"><span data-stu-id="b88c7-115">The name of the ANF account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b88c7-116">-AccountObject</span><span class="sxs-lookup"><span data-stu-id="b88c7-116">-AccountObject</span></span>
<span data-ttu-id="b88c7-117">新備份物件的帳戶</span><span class="sxs-lookup"><span data-stu-id="b88c7-117">The account for the new backup object</span></span>

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

### <span data-ttu-id="b88c7-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b88c7-118">-DefaultProfile</span></span>
<span data-ttu-id="b88c7-119">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="b88c7-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b88c7-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b88c7-120">-ResourceGroupName</span></span>
<span data-ttu-id="b88c7-121">ANF 帳戶的 [資源] 群組</span><span class="sxs-lookup"><span data-stu-id="b88c7-121">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="b88c7-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b88c7-122">-ResourceId</span></span>
<span data-ttu-id="b88c7-123">ANF 池的資源識別碼</span><span class="sxs-lookup"><span data-stu-id="b88c7-123">The resource id of the ANF pool</span></span>

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

### <span data-ttu-id="b88c7-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b88c7-124">CommonParameters</span></span>
<span data-ttu-id="b88c7-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b88c7-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b88c7-126">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="b88c7-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b88c7-127">輸入</span><span class="sxs-lookup"><span data-stu-id="b88c7-127">INPUTS</span></span>

### <span data-ttu-id="b88c7-128">PSNetAppFilesAccount 中的 NetAppFiles。</span><span class="sxs-lookup"><span data-stu-id="b88c7-128">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

### <span data-ttu-id="b88c7-129">System.object</span><span class="sxs-lookup"><span data-stu-id="b88c7-129">System.String</span></span>

## <span data-ttu-id="b88c7-130">輸出</span><span class="sxs-lookup"><span data-stu-id="b88c7-130">OUTPUTS</span></span>

### <span data-ttu-id="b88c7-131">PSNetAppFilesBackupPolicy 中的 NetAppFiles。</span><span class="sxs-lookup"><span data-stu-id="b88c7-131">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackupPolicy</span></span>

## <span data-ttu-id="b88c7-132">筆記</span><span class="sxs-lookup"><span data-stu-id="b88c7-132">NOTES</span></span>

## <span data-ttu-id="b88c7-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="b88c7-133">RELATED LINKS</span></span>
