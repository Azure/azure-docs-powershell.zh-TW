---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/powershell/module/az.netappfiles/get-aznetappfilesvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesVault.md
ms.openlocfilehash: d2741b3eb10618b9bdbe2e97b14d176c2b3eab26
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101906058"
---
# <span data-ttu-id="ecf71-101">Get-AzNetAppFilesVault</span><span class="sxs-lookup"><span data-stu-id="ecf71-101">Get-AzNetAppFilesVault</span></span>

## <span data-ttu-id="ecf71-102">簡介</span><span class="sxs-lookup"><span data-stu-id="ecf71-102">SYNOPSIS</span></span>
<span data-ttu-id="ecf71-103">從帳戶備份保存庫 (ANF) Azure NetApp 檔案清單。</span><span class="sxs-lookup"><span data-stu-id="ecf71-103">Gets list of Azure NetApp Files (ANF) Accounts backup vaults.</span></span>

## <span data-ttu-id="ecf71-104">語法</span><span class="sxs-lookup"><span data-stu-id="ecf71-104">SYNTAX</span></span>

### <span data-ttu-id="ecf71-105">ByFieldsParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="ecf71-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzNetAppFilesVault -ResourceGroupName <String> [-AccountName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ecf71-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ecf71-106">ByParentObjectParameterSet</span></span>
```
Get-AzNetAppFilesVault -AccountObject <PSNetAppFilesAccount> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ecf71-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ecf71-107">ByResourceIdParameterSet</span></span>
```
Get-AzNetAppFilesVault -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ecf71-108">描述</span><span class="sxs-lookup"><span data-stu-id="ecf71-108">DESCRIPTION</span></span>
<span data-ttu-id="ecf71-109">**Get-AzNetAppFilesVault** Cmdlet 會取得 ANF 帳戶備份庫的清單。</span><span class="sxs-lookup"><span data-stu-id="ecf71-109">The **Get-AzNetAppFilesVault** cmdlet gets list of an ANF accounts backup vaults.</span></span>

## <span data-ttu-id="ecf71-110">例子</span><span class="sxs-lookup"><span data-stu-id="ecf71-110">EXAMPLES</span></span>

### <span data-ttu-id="ecf71-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="ecf71-111">Example 1</span></span>
```powershell
PS C:\> Get-AzNetAppFilesVault -ResourceGroupName "MyRG" -AccountName "MyAnfAccount"
```

<span data-ttu-id="ecf71-112">此命令會獲得 Azure NetappFiles 的備份庫清單 (ANF) 帳戶 "MyAnfAccount"。</span><span class="sxs-lookup"><span data-stu-id="ecf71-112">This command gets a list of the backup vaults for Azure NetappFiles (ANF) account "MyAnfAccount".</span></span>

## <span data-ttu-id="ecf71-113">參數</span><span class="sxs-lookup"><span data-stu-id="ecf71-113">PARAMETERS</span></span>

### <span data-ttu-id="ecf71-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="ecf71-114">-AccountName</span></span>
<span data-ttu-id="ecf71-115">ANF 帳戶的名稱</span><span class="sxs-lookup"><span data-stu-id="ecf71-115">The name of the ANF account</span></span>

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

### <span data-ttu-id="ecf71-116">-AccountObject</span><span class="sxs-lookup"><span data-stu-id="ecf71-116">-AccountObject</span></span>
<span data-ttu-id="ecf71-117">新備份物件的帳戶</span><span class="sxs-lookup"><span data-stu-id="ecf71-117">The account for the new backup object</span></span>

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

### <span data-ttu-id="ecf71-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ecf71-118">-DefaultProfile</span></span>
<span data-ttu-id="ecf71-119">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="ecf71-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ecf71-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ecf71-120">-ResourceGroupName</span></span>
<span data-ttu-id="ecf71-121">ANF 帳戶的資源群組</span><span class="sxs-lookup"><span data-stu-id="ecf71-121">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="ecf71-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ecf71-122">-ResourceId</span></span>
<span data-ttu-id="ecf71-123">ANF 資料庫的資源識別碼</span><span class="sxs-lookup"><span data-stu-id="ecf71-123">The resource id of the ANF pool</span></span>

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

### <span data-ttu-id="ecf71-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ecf71-124">CommonParameters</span></span>
<span data-ttu-id="ecf71-125">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="ecf71-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ecf71-126">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ecf71-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ecf71-127">輸入</span><span class="sxs-lookup"><span data-stu-id="ecf71-127">INPUTS</span></span>

### <span data-ttu-id="ecf71-128">Microsoft.Azure.Commands.NetAppFiles.models.PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="ecf71-128">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

### <span data-ttu-id="ecf71-129">System.String</span><span class="sxs-lookup"><span data-stu-id="ecf71-129">System.String</span></span>

## <span data-ttu-id="ecf71-130">輸出</span><span class="sxs-lookup"><span data-stu-id="ecf71-130">OUTPUTS</span></span>

### <span data-ttu-id="ecf71-131">Microsoft.Azure.Commands.NetAppFiles.models.PSNetAppFilesBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="ecf71-131">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackupPolicy</span></span>

## <span data-ttu-id="ecf71-132">筆記</span><span class="sxs-lookup"><span data-stu-id="ecf71-132">NOTES</span></span>

## <span data-ttu-id="ecf71-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="ecf71-133">RELATED LINKS</span></span>
