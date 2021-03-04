---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: E2A56E55-30A3-4A2F-80AE-9D166840909E
online version: https://docs.microsoft.com/powershell/module/az.compute/get-azremotedesktopfile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzRemoteDesktopFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzRemoteDesktopFile.md
ms.openlocfilehash: d06f8b5efa0a220b20c5324b457a870d5aaa44b2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101909186"
---
# <span data-ttu-id="5e0e0-101">Get-AzRemoteDesktopFile</span><span class="sxs-lookup"><span data-stu-id="5e0e0-101">Get-AzRemoteDesktopFile</span></span>

## <span data-ttu-id="5e0e0-102">簡介</span><span class="sxs-lookup"><span data-stu-id="5e0e0-102">SYNOPSIS</span></span>
<span data-ttu-id="5e0e0-103">獲得 .rdp 檔案。</span><span class="sxs-lookup"><span data-stu-id="5e0e0-103">Gets an .rdp file.</span></span>

## <span data-ttu-id="5e0e0-104">語法</span><span class="sxs-lookup"><span data-stu-id="5e0e0-104">SYNTAX</span></span>

### <span data-ttu-id="5e0e0-105">下載</span><span class="sxs-lookup"><span data-stu-id="5e0e0-105">Download</span></span>
```
Get-AzRemoteDesktopFile [-ResourceGroupName] <String> [-Name] <String> [-LocalPath] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5e0e0-106">發射</span><span class="sxs-lookup"><span data-stu-id="5e0e0-106">Launch</span></span>
```
Get-AzRemoteDesktopFile [-ResourceGroupName] <String> [-Name] <String> [[-LocalPath] <String>] [-Launch]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5e0e0-107">描述</span><span class="sxs-lookup"><span data-stu-id="5e0e0-107">DESCRIPTION</span></span>
<span data-ttu-id="5e0e0-108">**Get-AzRemoteDesktopFile** Cmdlet 會取得遠端桌面通訊協定 (.rdp) 檔案。</span><span class="sxs-lookup"><span data-stu-id="5e0e0-108">The **Get-AzRemoteDesktopFile** cmdlet gets a Remote Desktop Protocol (.rdp) file.</span></span>

## <span data-ttu-id="5e0e0-109">例子</span><span class="sxs-lookup"><span data-stu-id="5e0e0-109">EXAMPLES</span></span>

### <span data-ttu-id="5e0e0-110">範例 1：取得遠端桌面檔案</span><span class="sxs-lookup"><span data-stu-id="5e0e0-110">Example 1: Get a Remote Desktop file</span></span>
```
PS C:\> Get-AzRemoteDesktopFile -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07" -LocalPath "D:\RemoteDesktopFile07.rdp"
```

<span data-ttu-id="5e0e0-111">此命令會針對名為 VirtualMachine07 的虛擬機器，獲得遠端桌面檔案。</span><span class="sxs-lookup"><span data-stu-id="5e0e0-111">This command gets the Remote Desktop file for the virtual machine named VirtualMachine07.</span></span>
<span data-ttu-id="5e0e0-112">該命令將結果儲存在名為 D：\RemoteDesktopFile07.rdp 的檔案中。</span><span class="sxs-lookup"><span data-stu-id="5e0e0-112">The command stores the result in the file named D:\RemoteDesktopFile07.rdp.</span></span>

## <span data-ttu-id="5e0e0-113">參數</span><span class="sxs-lookup"><span data-stu-id="5e0e0-113">PARAMETERS</span></span>

### <span data-ttu-id="5e0e0-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e0e0-114">-DefaultProfile</span></span>
<span data-ttu-id="5e0e0-115">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="5e0e0-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5e0e0-116">-啟動</span><span class="sxs-lookup"><span data-stu-id="5e0e0-116">-Launch</span></span>
<span data-ttu-id="5e0e0-117">表示此 Cmdlet 在獲得 .rdp 檔案後，會啟動遠端桌面。</span><span class="sxs-lookup"><span data-stu-id="5e0e0-117">Indicates that this cmdlet launches Remote Desktop after it gets the .rdp file.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Launch
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e0e0-118">-LocalPath</span><span class="sxs-lookup"><span data-stu-id="5e0e0-118">-LocalPath</span></span>
<span data-ttu-id="5e0e0-119">指定此 Cmdlet 儲存 .rdp 檔案的當地完整路徑。</span><span class="sxs-lookup"><span data-stu-id="5e0e0-119">Specifies the local full path where this cmdlet stores the .rdp file.</span></span>

```yaml
Type: System.String
Parameter Sets: Download
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Launch
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5e0e0-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="5e0e0-120">-Name</span></span>
<span data-ttu-id="5e0e0-121">指定此 Cmdlet 獲得的可用性集名稱。</span><span class="sxs-lookup"><span data-stu-id="5e0e0-121">Specifies the name of the availability set that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName, VMName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5e0e0-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5e0e0-122">-ResourceGroupName</span></span>
<span data-ttu-id="5e0e0-123">指定資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="5e0e0-123">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5e0e0-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e0e0-124">CommonParameters</span></span>
<span data-ttu-id="5e0e0-125">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="5e0e0-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e0e0-126">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5e0e0-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e0e0-127">輸入</span><span class="sxs-lookup"><span data-stu-id="5e0e0-127">INPUTS</span></span>

### <span data-ttu-id="5e0e0-128">System.String</span><span class="sxs-lookup"><span data-stu-id="5e0e0-128">System.String</span></span>

## <span data-ttu-id="5e0e0-129">輸出</span><span class="sxs-lookup"><span data-stu-id="5e0e0-129">OUTPUTS</span></span>

### <span data-ttu-id="5e0e0-130">System.Void</span><span class="sxs-lookup"><span data-stu-id="5e0e0-130">System.Void</span></span>

## <span data-ttu-id="5e0e0-131">筆記</span><span class="sxs-lookup"><span data-stu-id="5e0e0-131">NOTES</span></span>

## <span data-ttu-id="5e0e0-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="5e0e0-132">RELATED LINKS</span></span>
