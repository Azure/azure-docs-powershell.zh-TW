---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/powershell/module/az.netappfiles/get-aznetappfilesactivedirectory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesActiveDirectory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesActiveDirectory.md
ms.openlocfilehash: 7198e34e7e888c2e89fce6cb5293bfc46bf57b1e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101906082"
---
# <span data-ttu-id="5c7d0-101">Get-AzNetAppFilesActiveDirectory</span><span class="sxs-lookup"><span data-stu-id="5c7d0-101">Get-AzNetAppFilesActiveDirectory</span></span>

## <span data-ttu-id="5c7d0-102">簡介</span><span class="sxs-lookup"><span data-stu-id="5c7d0-102">SYNOPSIS</span></span>
<span data-ttu-id="5c7d0-103">在 Active Directory 組 (ANF 中) Azure NetApp 檔案的詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="5c7d0-103">Gets details of an Azure NetApp Files (ANF) Active Directory configuration.</span></span>

## <span data-ttu-id="5c7d0-104">語法</span><span class="sxs-lookup"><span data-stu-id="5c7d0-104">SYNTAX</span></span>

### <span data-ttu-id="5c7d0-105">ByFieldsParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="5c7d0-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzNetAppFilesActiveDirectory -ResourceGroupName <String> -AccountName <String>
 [-ActiveDirectoryId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5c7d0-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5c7d0-106">ByParentObjectParameterSet</span></span>
```
Get-AzNetAppFilesActiveDirectory [-ActiveDirectoryId <String>] -AccountObject <PSNetAppFilesAccount>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5c7d0-107">描述</span><span class="sxs-lookup"><span data-stu-id="5c7d0-107">DESCRIPTION</span></span>
<span data-ttu-id="5c7d0-108">**Get-AzNetAppFilesActiveDirectory Cmdlet** 會取得 ANF 帳戶 Active Directory 組式的詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="5c7d0-108">The **Get-AzNetAppFilesActiveDirectory** cmdlet gets details of an ANF accounts Active Directory configuration.</span></span>

## <span data-ttu-id="5c7d0-109">例子</span><span class="sxs-lookup"><span data-stu-id="5c7d0-109">EXAMPLES</span></span>

### <span data-ttu-id="5c7d0-110">範例 1</span><span class="sxs-lookup"><span data-stu-id="5c7d0-110">Example 1</span></span>
```powershell
PS C:\> Get-AzNetAppFilesActiveDirectory -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -Name "MyADConfigName"
```

<span data-ttu-id="5c7d0-111">此命令會針對名為 MyAnfAccount 的 ANF (帳戶) 名稱為 MyADConfigName 的 AD 組配置。</span><span class="sxs-lookup"><span data-stu-id="5c7d0-111">This command gets the AD configuration named MyADConfigName for the Azure NetApp Files (ANF) account named MyAnfAccount.</span></span>

## <span data-ttu-id="5c7d0-112">參數</span><span class="sxs-lookup"><span data-stu-id="5c7d0-112">PARAMETERS</span></span>

### <span data-ttu-id="5c7d0-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="5c7d0-113">-AccountName</span></span>
<span data-ttu-id="5c7d0-114">ANF 帳戶的名稱</span><span class="sxs-lookup"><span data-stu-id="5c7d0-114">The name of the ANF account</span></span>

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

### <span data-ttu-id="5c7d0-115">-AccountObject</span><span class="sxs-lookup"><span data-stu-id="5c7d0-115">-AccountObject</span></span>
<span data-ttu-id="5c7d0-116">新 Active Directory 物件的帳戶</span><span class="sxs-lookup"><span data-stu-id="5c7d0-116">The Account for the new Active Directory object</span></span>

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

### <span data-ttu-id="5c7d0-117">-ActiveDirectoryId</span><span class="sxs-lookup"><span data-stu-id="5c7d0-117">-ActiveDirectoryId</span></span>
<span data-ttu-id="5c7d0-118">ANF Active Directory 的 ActiveDirectoryId</span><span class="sxs-lookup"><span data-stu-id="5c7d0-118">The ActiveDirectoryId of the ANF Active Directory</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ActiveDirectoryName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c7d0-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5c7d0-119">-DefaultProfile</span></span>
<span data-ttu-id="5c7d0-120">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="5c7d0-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5c7d0-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5c7d0-121">-ResourceGroupName</span></span>
<span data-ttu-id="5c7d0-122">ANF 帳戶的資源群組</span><span class="sxs-lookup"><span data-stu-id="5c7d0-122">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="5c7d0-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c7d0-123">CommonParameters</span></span>
<span data-ttu-id="5c7d0-124">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="5c7d0-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c7d0-125">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5c7d0-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c7d0-126">輸入</span><span class="sxs-lookup"><span data-stu-id="5c7d0-126">INPUTS</span></span>

### <span data-ttu-id="5c7d0-127">Microsoft.Azure.Commands.NetAppFiles.models.PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="5c7d0-127">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="5c7d0-128">輸出</span><span class="sxs-lookup"><span data-stu-id="5c7d0-128">OUTPUTS</span></span>

### <span data-ttu-id="5c7d0-129">Microsoft.Azure.Commands.NetAppFiles.models.PSNetAppFilesActiveDirectory</span><span class="sxs-lookup"><span data-stu-id="5c7d0-129">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesActiveDirectory</span></span>

## <span data-ttu-id="5c7d0-130">筆記</span><span class="sxs-lookup"><span data-stu-id="5c7d0-130">NOTES</span></span>

## <span data-ttu-id="5c7d0-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="5c7d0-131">RELATED LINKS</span></span>
