---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/powershell/module/az.netappfiles/get-aznetappfilesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesAccount.md
ms.openlocfilehash: 9741a150dd26e3fef513984fa4ae8b6a2e7c97b9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101906086"
---
# <span data-ttu-id="44ee4-101">Get-AzNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="44ee4-101">Get-AzNetAppFilesAccount</span></span>

## <span data-ttu-id="44ee4-102">簡介</span><span class="sxs-lookup"><span data-stu-id="44ee4-102">SYNOPSIS</span></span>
<span data-ttu-id="44ee4-103">從 ANF 帳戶 (Azure NetApp 檔案) 詳細資料。</span><span class="sxs-lookup"><span data-stu-id="44ee4-103">Gets details of an Azure NetApp Files (ANF) account.</span></span>

## <span data-ttu-id="44ee4-104">語法</span><span class="sxs-lookup"><span data-stu-id="44ee4-104">SYNTAX</span></span>

### <span data-ttu-id="44ee4-105">ByFieldsParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="44ee4-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzNetAppFilesAccount -ResourceGroupName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="44ee4-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="44ee4-106">ByResourceIdParameterSet</span></span>
```
Get-AzNetAppFilesAccount -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="44ee4-107">描述</span><span class="sxs-lookup"><span data-stu-id="44ee4-107">DESCRIPTION</span></span>
<span data-ttu-id="44ee4-108">**Get-AzNetAppFilesAccount** Cmdlet 會取得 ANF 帳戶的詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="44ee4-108">The **Get-AzNetAppFilesAccount** cmdlet gets details of an ANF account.</span></span>

## <span data-ttu-id="44ee4-109">例子</span><span class="sxs-lookup"><span data-stu-id="44ee4-109">EXAMPLES</span></span>

### <span data-ttu-id="44ee4-110">範例 1：取得 ANF 帳戶</span><span class="sxs-lookup"><span data-stu-id="44ee4-110">Example 1: Get an ANF account</span></span>
```
PS C:\>Get-AzNetAppFilesAccount -ResourceGroupName "MyRG" -Name "MyAnfAccount"

Output:

Location          : westus2
Id                : /subscriptions/mySubs/resourceGroups/MyRG/providers/Microsoft.NetApp/netAppAccounts/MyAnfAccount
Name              : MyAnfAccount
Type              : Microsoft.NetApp/netAppAccounts
Tags              :
ProvisioningState : Succeeded
```

<span data-ttu-id="44ee4-111">此命令會獲得名為 MyAnfAccount 的帳戶。</span><span class="sxs-lookup"><span data-stu-id="44ee4-111">This command gets the account named MyAnfAccount.</span></span>

## <span data-ttu-id="44ee4-112">參數</span><span class="sxs-lookup"><span data-stu-id="44ee4-112">PARAMETERS</span></span>

### <span data-ttu-id="44ee4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="44ee4-113">-DefaultProfile</span></span>
<span data-ttu-id="44ee4-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="44ee4-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="44ee4-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="44ee4-115">-Name</span></span>
<span data-ttu-id="44ee4-116">ANF 帳戶的名稱</span><span class="sxs-lookup"><span data-stu-id="44ee4-116">The name of the ANF account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases: AccountName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44ee4-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="44ee4-117">-ResourceGroupName</span></span>
<span data-ttu-id="44ee4-118">ANF 帳戶的資源群組</span><span class="sxs-lookup"><span data-stu-id="44ee4-118">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="44ee4-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="44ee4-119">-ResourceId</span></span>
<span data-ttu-id="44ee4-120">ANF 帳戶的資源識別碼</span><span class="sxs-lookup"><span data-stu-id="44ee4-120">The resource id of the ANF account</span></span>

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

### <span data-ttu-id="44ee4-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44ee4-121">CommonParameters</span></span>
<span data-ttu-id="44ee4-122">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="44ee4-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44ee4-123">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="44ee4-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44ee4-124">輸入</span><span class="sxs-lookup"><span data-stu-id="44ee4-124">INPUTS</span></span>

### <span data-ttu-id="44ee4-125">System.String</span><span class="sxs-lookup"><span data-stu-id="44ee4-125">System.String</span></span>

## <span data-ttu-id="44ee4-126">輸出</span><span class="sxs-lookup"><span data-stu-id="44ee4-126">OUTPUTS</span></span>

### <span data-ttu-id="44ee4-127">Microsoft.Azure.Commands.NetAppFiles.models.PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="44ee4-127">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="44ee4-128">筆記</span><span class="sxs-lookup"><span data-stu-id="44ee4-128">NOTES</span></span>

## <span data-ttu-id="44ee4-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="44ee4-129">RELATED LINKS</span></span>
