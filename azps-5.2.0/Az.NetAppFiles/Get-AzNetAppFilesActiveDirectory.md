---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/get-aznetappfilesactivedirectory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesActiveDirectory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesActiveDirectory.md
ms.openlocfilehash: 6c082d2e61f81c4e0b8cf9bebefd623584fac3e9
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98281788"
---
# <span data-ttu-id="980ce-101">Get-AzNetAppFilesActiveDirectory</span><span class="sxs-lookup"><span data-stu-id="980ce-101">Get-AzNetAppFilesActiveDirectory</span></span>

## <span data-ttu-id="980ce-102">摘要</span><span class="sxs-lookup"><span data-stu-id="980ce-102">SYNOPSIS</span></span>
<span data-ttu-id="980ce-103">取得 Azure NetApp 檔案 (ANF) Active Directory 設定的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="980ce-103">Gets details of an Azure NetApp Files (ANF) Active Directory configuration.</span></span>

## <span data-ttu-id="980ce-104">句法</span><span class="sxs-lookup"><span data-stu-id="980ce-104">SYNTAX</span></span>

### <span data-ttu-id="980ce-105">ByFieldsParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="980ce-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzNetAppFilesActiveDirectory -ResourceGroupName <String> -AccountName <String>
 [-ActiveDirectoryId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="980ce-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="980ce-106">ByParentObjectParameterSet</span></span>
```
Get-AzNetAppFilesActiveDirectory [-ActiveDirectoryId <String>] -AccountObject <PSNetAppFilesAccount>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="980ce-107">說明</span><span class="sxs-lookup"><span data-stu-id="980ce-107">DESCRIPTION</span></span>
<span data-ttu-id="980ce-108">**AzNetAppFilesActiveDirectory** Cmdlet 會取得 ANF 帳戶 Active Directory 設定的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="980ce-108">The **Get-AzNetAppFilesActiveDirectory** cmdlet gets details of an ANF accounts Active Directory configuration.</span></span>

## <span data-ttu-id="980ce-109">示例</span><span class="sxs-lookup"><span data-stu-id="980ce-109">EXAMPLES</span></span>

### <span data-ttu-id="980ce-110">範例1</span><span class="sxs-lookup"><span data-stu-id="980ce-110">Example 1</span></span>
```powershell
PS C:\> Get-AzNetAppFilesActiveDirectory -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -Name "MyADConfigName"
```

<span data-ttu-id="980ce-111">這個命令會取得 Azure NetApp 檔案的名為 MyADConfigName 的 AD 設定， (ANF 名為 MyAnfAccount 的) 帳戶。</span><span class="sxs-lookup"><span data-stu-id="980ce-111">This command gets the AD configuration named MyADConfigName for the Azure NetApp Files (ANF) account named MyAnfAccount.</span></span>

## <span data-ttu-id="980ce-112">參數</span><span class="sxs-lookup"><span data-stu-id="980ce-112">PARAMETERS</span></span>

### <span data-ttu-id="980ce-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="980ce-113">-AccountName</span></span>
<span data-ttu-id="980ce-114">ANF 帳戶的名稱</span><span class="sxs-lookup"><span data-stu-id="980ce-114">The name of the ANF account</span></span>

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

### <span data-ttu-id="980ce-115">-AccountObject</span><span class="sxs-lookup"><span data-stu-id="980ce-115">-AccountObject</span></span>
<span data-ttu-id="980ce-116">新 Active Directory 物件的帳戶</span><span class="sxs-lookup"><span data-stu-id="980ce-116">The Account for the new Active Directory object</span></span>

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

### <span data-ttu-id="980ce-117">-ActiveDirectoryId</span><span class="sxs-lookup"><span data-stu-id="980ce-117">-ActiveDirectoryId</span></span>
<span data-ttu-id="980ce-118">ANF Active Directory 的 ActiveDirectoryId</span><span class="sxs-lookup"><span data-stu-id="980ce-118">The ActiveDirectoryId of the ANF Active Directory</span></span>

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

### <span data-ttu-id="980ce-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="980ce-119">-DefaultProfile</span></span>
<span data-ttu-id="980ce-120">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="980ce-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="980ce-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="980ce-121">-ResourceGroupName</span></span>
<span data-ttu-id="980ce-122">ANF 帳戶的 [資源] 群組</span><span class="sxs-lookup"><span data-stu-id="980ce-122">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="980ce-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="980ce-123">CommonParameters</span></span>
<span data-ttu-id="980ce-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="980ce-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="980ce-125">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="980ce-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="980ce-126">輸入</span><span class="sxs-lookup"><span data-stu-id="980ce-126">INPUTS</span></span>

### <span data-ttu-id="980ce-127">PSNetAppFilesAccount 中的 NetAppFiles。</span><span class="sxs-lookup"><span data-stu-id="980ce-127">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="980ce-128">輸出</span><span class="sxs-lookup"><span data-stu-id="980ce-128">OUTPUTS</span></span>

### <span data-ttu-id="980ce-129">PSNetAppFilesActiveDirectory 中的 NetAppFiles。</span><span class="sxs-lookup"><span data-stu-id="980ce-129">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesActiveDirectory</span></span>

## <span data-ttu-id="980ce-130">筆記</span><span class="sxs-lookup"><span data-stu-id="980ce-130">NOTES</span></span>

## <span data-ttu-id="980ce-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="980ce-131">RELATED LINKS</span></span>
